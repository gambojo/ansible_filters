```yaml
- name: Merge lists
  ansible.builtin.include_role:
    name: ansible_filters
    tasks_from: merge-lists-with-key-value-dicts.yml
```
