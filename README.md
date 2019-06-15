# zulip-emoji-import

Helpful links:

- https://github.com/ruchit2801/zulip/commit/721664581d36baa85ce4f93a1ed3c10bc72c0ee7
- https://github.com/zulip/zulip/commit/3eeec94d036c606942bfa2ed17d8488417ffc312
- https://zulip.readthedocs.io/en/latest/tutorials/documenting-api-endpoints.html




https://slackmojis.com/



```
for i in $(curl -s https://slackmojis.com/ | awk -F\" '/href=.*images/ { print $2; }' | sed -e s/\?.\*//); do (curl -s $i > $(echo $i | sed s/[:/]/-/g); echo $i)& done
```
