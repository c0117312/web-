# git�̑���ŕ�����Ȃ�����������������md


1. ���߂ă��|�W�g���쐬���ɓo�^��rejecte����

* �菇����
  
github���ɏ��߂ă��|�W�g�����쐬

Git bush�Ń��|�W�g���ɋ��������t�@�C���̏ꏊ��
  ```
  git init
  ```
����ă��|�W�g��(���[�J��)�����

�����Ĉȉ��̎菇�𓥂�

```
git add �ǉ�����t�@�C��

git commit -m "�R�����g"

git remote add origin �ǉ����郊�|�W�g����URL
```

�����܂ł͖��Ȃ��B���͎��ɔ���

```
git push origin master
```
����ƈȉ��̃G���[���\��

```
To https://github.com/c0117312/web-
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/c0117312/web-'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

* ������������

����github�̃��|�W�g�����쐬�������AREADME.md���ǉ��������A���ꂪ���[�J�����ɔF������Ă��Ȃ��̂ŁAreject���ꂽ�B

* �������@

����͈ȉ��̒ʂ�B�܂�fetch���鎖�Ń��[�J����README��ǉ�����B

```
git fetch
```

�X��**merge**����B���̎��� **--allow-unrelated-histories** �̃I�v�V������ǉ�����B����͖{���}�[�W���鎞�̋��ʂ̕��򌳂������Ȃ��u�����`���}�[�W����B

```
git merge --allow-unrelated-histories origin/master
```

�����܂ŗ������͂�����

```
git push orgin master
```
���̖��͏I��




