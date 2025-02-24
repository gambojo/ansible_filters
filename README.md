### Example
```yaml
- hosts: localhost
  vars:
    list1:
      - name: "key-1"
        option: "value-1"
      - name: "key-2"
        option: "value-2"
      - name: "key-3"
        option: "value-3"

    list2:
      - name: "key-1"
        option: "custom-value-1"
      - name: "key-2"
        option: "custom-value-2"

    source_list: "{{ list1 }}"
    custom_list: "{{ list2 }}"

  tasks:
    - name: Merge lists
      ansible.builtin.include_role:
        name: ansible_filters
        tasks_from: merge-lists-with-key-value-dicts.yml

    - name: Print result
      debug:
        msg: "{{ merged_list }}"
```

