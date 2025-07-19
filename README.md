# manifests

We're using [repo](https://source.android.com/docs/setup/reference/repo) to manage BlueOS kernel project.
Use following command to download and install `repo`.
```
export REPO_URL=https://mirrors.tuna.tsinghua.edu.cn/git/git-repo
mkdir -p ~/.local/bin
curl ${REPO_URL} -o ~/.local/bin/repo
chmod +x ~/.local/bin/repo
echo "export REPO_URL=https://mirrors.tuna.tsinghua.edu.cn/git/git-repo" >> ${HOME}/.bashrc
```
Make sure `${HOME}/.local/bin` is in your `${PATH}`.

BlueOS kernel project is consisted with multiple repositories. Use folloing command to fetch these repos.
```bash
mkdir blueos-dev
cd blueos-dev
repo init -u git@github.com:vivoblueos/manifests.git -b main -m manifest.xml && repo sync
```
Next, please follow instructions on the [vivo BlueOS kernel book](https://github.com/vivoblueos/book/blob/main/src/SUMMARY.md)
to build the vivo BlueOS kernel book and start your development career.
