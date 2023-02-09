# SSH Commands
## File Transfers
* `scp [USERNAME@remote_IP:dir_to_file] [local_path]` | secure copy from remote to local (pull) 
* `scp [local_path] [USERNAME@remote_IP:dir_to_file]` | secure copy from local to remote (push)

## SFTP
* `sftp [USERNAME@remote_IP]` | login to remote terminal
  * Place an `l` before any command to run it on the local machine.
    * `lcd [dir]` | change local directory
    * `lls` | view local files
* `put [file]` | upload the file from local to remote
* `get [file]` | download the file from remote to local

## Local Web Server
* `sudo python3 -m http.server 99` | creates a local server
  * This website can be accessed at `local_IP:99`.
  * This provides a view of all the websites in the directory the web server was launched in.
