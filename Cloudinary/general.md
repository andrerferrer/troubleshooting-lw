[back](../README.md)

- issue seeding pictures from Cloudinary

```
Error:
tempfile error (on Ubuntu). 

Fix:
item.individual_pieces.attach(
    io: open('https://res.cloudinary.com/dj9iphc8u/image/upload/v1597913613/outfit/o1_sweater_a94vol.png'),
    filename: 'o1_sweater_a94vol.png',
    content_type: 'image/png',
    identify: false
  )

Adding the identify: false fixed the issue
```