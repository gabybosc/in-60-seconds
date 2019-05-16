# Let's Get Started

---

## Add Some Slide Candy

![](assets/img/presentation.png)

---
@title[Customize Slide Layout]

@snap[west span-50]
## Customize Slide Content Layout

for indice, l in enumerate(orbitas):
        calendario[i*5+indice,0] = mag[1,1]
        calendario[i*5+indice,1] = indice+1
        pos = l * 3390
        X_MSO = pos[:, 0]
        Z_MSO = pos[:, 2]
        idx_min = np.zeros(int(una_vuelta/paso))
        max_acercamiento = np.zeros(int(una_vuelta/paso))
        minimo = 0
        for k in range(int(una_vuelta)-100):
            if k%paso == 0 and Z_MSO[k] > 0 and X_MSO[k] > 0:
                for m in range(len(R)):
                    resta[m, :] = l[k,:] - R[m,:]
                A = np.linalg.norm(resta, axis=1)
                idx_min[int(k/paso)] = np.argmin(A)
                max_acercamiento[int(k/paso)] = A[int(idx_min[int(k/paso)])]
        if sum(max_acercamiento) == 0: #si es cero, va a fallar todo el script, así que digo que esa órbita es mala y listo
            calendario[i*5+indice,2] = 0
            calendario[i*5+indice, 3] = 0
            calendario[i*5+indice,4] = 0
        else:
            minimo = np.where( max_acercamiento==np.min(max_acercamiento[np.nonzero(max_acercamiento)]))[0][0] #busca el minimo que no sea cero

@snapend

@snap[east span-50]
![](assets/img/presentation.png)
@snapend

---?color=#E58537
@title[Add A Little Imagination]

@snap[north-west]
#### Add a splash of @color[cyan](**color**) and you are ready to start presenting...
@snapend

@snap[west span-55]
@ul[spaced text-white]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 headline]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
