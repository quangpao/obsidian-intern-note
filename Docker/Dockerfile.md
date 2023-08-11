Docker tạo ra các [[Docker Image]] bằng cách đọc **Dockerfile**. **Dockerfile** là một document bao gồm tất cả các lệnh mà một người dùng có thể gọi để tạo ra *image*. 

### Dockerfile Format:
```dockerfile
#comment
INSTRUCTION arguments
```


Example:
```dockerfile
FROM       python:3
LABEL      maintainer="Sawood Alam <@ibnesayeed>"

WORKDIR    /app
COPY       requirements.txt /app/
RUN        pip install -r requirements.txt

COPY       *.py /app/
RUN        chmod a+x *.py

CMD        ["./main.py"]
```