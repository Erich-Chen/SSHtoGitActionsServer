Removed all jobs but the ability to ssh to the git actions server.

````
    - name: SSH connection to Actions
      uses: P3TERX/ssh2actions@v1.0.0
      if: (github.event.inputs.ssh == 'true' && github.event.inputs.ssh  != 'false') || contains(github.event.action, 'ssh')
      env:
        TELEGRAM_CHAT_ID: ${{ secrets.TELEGRAM_CHAT_ID }}
        TELEGRAM_BOT_TOKEN: ${{ secrets.TELEGRAM_BOT_TOKEN }}
````
