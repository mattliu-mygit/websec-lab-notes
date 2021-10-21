# Web Security Lab - Notes

# Setup

1. Install Node.js.
2. `cd` into the `src` folder, and run `npm install`.
3. Run `node app.js`.
4. Go to `http://localhost:80` in your browser.

Alternatively, you can use Docker:

    docker-compose up -d
    open http://127.0.0.1:8083/

# Experiments

This challenges have three vulnerabilities: OS command injection, prototype pollution and path traversal. Your task is to find out what you can do with these vulnerabilities.


curl -d "author='Matt'&raw='hello'" -X POST http://localhost:80/add_note

curl -X POST http://localhost:8000/mattliu-mygit/obj_name \
     -d '{ foo: "bar" }'

     curl -X GET http://localhost:80/img?id=../app.js
     curl -X GET http://localhost:80/img?id=../../../../../../../Windows/system32/drivers/etc/hosts
