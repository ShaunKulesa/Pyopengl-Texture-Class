Usage:
```py
texture1 = Texture("image1")
texture2 = Texture("image2")

texture1.bind()
texture2.bind()
```

Example:
```py
texture1 = Texture("image1")
texture2 = Texture("image2")

GL.glEnable(GL.GL_BLEND)
GL.glBlendFunc(GL.GL_SRC_ALPHA, GL.GL_ONE_MINUS_SRC_ALPHA)
GL.glEnable(GL.GL_TEXTURE_2D)
texture1.bind()
GL.glBegin(GL.GL_QUADS)
GL.glTexCoord2f(0, 0)
GL.glVertex2f(200, 300)
GL.glTexCoord2f(0, 1)
GL.glVertex2f(200, 100)
GL.glTexCoord2f(1, 1)
GL.glVertex2f(300, 100)
GL.glTexCoord2f(1, 0)
GL.glVertex2f(300, 300)
GL.glEnd()
GL.glDisable(GL.GL_TEXTURE_2D)

GL.glEnable(GL.GL_BLEND)
GL.glBlendFunc(GL.GL_SRC_ALPHA, GL.GL_ONE_MINUS_SRC_ALPHA)
GL.glEnable(GL.GL_TEXTURE_2D)
texture2.bind()
GL.glBegin(GL.GL_QUADS)
GL.glTexCoord2f(0, 0)
GL.glVertex2f(400, 300)
GL.glTexCoord2f(0, 1)
GL.glVertex2f(400, 100)
GL.glTexCoord2f(1, 1)
GL.glVertex2f(500, 100)
GL.glTexCoord2f(1, 0)
GL.glVertex2f(500, 300)
GL.glEnd()
GL.glDisable(GL.GL_TEXTURE_2D)
```
