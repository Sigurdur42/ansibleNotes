´´´
  - name: Add flathub remote
    community.general.flatpak_remote:
      name: flathub
      state: present
      flatpakrepo_url: https://flathub.org/repo/flathub.flatpakrepo

  - name: Install flatpaks
    community.general.flatpak:
      name: "{{ flatpaks_to_install }}"
      state: latest
´´´