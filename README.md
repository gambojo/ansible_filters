### Example
```yaml
- hosts: localhost
  tasks:
    - name: Merge lists
      ansible.builtin.include_role:
        name: ansible_filters
        tasks_from: merge-lists-with-key-value-dicts.yml

    - name: Print result
      debug:
        msg: "{{ merged_list }}"
```

