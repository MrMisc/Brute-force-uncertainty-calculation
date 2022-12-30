
@client.command()
@commands.has_any_role('Duke', 'Moderator', 'Tsuki')
async def unc(ctx, arg1, arg2, *args):
    n = len(args)
    Number = int(arg2.strip())
    limit = Number ** n
    if limit >=45000001:
        await ctx.send('No can do because arg2^no.(vectors) is greater than 45 million!')
        if "duke" in [y.name.lower() for y in ctx.author.roles]:

            tsundere = await client.wait_for('message', timeout = 5.0, check = lambda message: message.author == ctx.author)
            tsun = tsundere.content
            if '0verride' or 'Override' in tsun:
                await ctx.send('UwU')
                await ctx.send(f'RIP. See ya in {limit/45E6 * 12.6}min')
                await ctx.send('https://66.media.tumblr.com/07e66b40902c48b64f603a4277ebdd71/tumblr_ouiyulleIv1s32c21o1_400.gif')
        else:
            return

    G = arg1.strip()
    Vs = []
    m = []
    err = []
    for Tp in args:
        Vs.append(Tp.strip().split(','))
    for V in Vs:
        m.append(float(V[0]))
        err.append(float(V[1]))

    v = []
    for i in range(n):
        low = m[i] - err[i]
        high = m[i] + err[i]
        v.append(np.linspace(low, high, Number))
        # print(v[0])

    # print(v)
    # print(v[0][1])

    all_perms = []
    answer = []
    TRUEanswer = []
    def brute_force(ls, indx, total, Vs):
    #ls must be empty list []
    #indx must be 0
    #total must be the number of vectors
    #print(f"{indx}/{total}")
        if len(answer)>1: return
        if indx>=total:
            all_perms.append(ls)
            if n == 3:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            x1 = float(v[0][i])
                            x2 = float(v[1][j])
                            x3 = float(v[2][k])
                            f = ne.evaluate(G)
                            fv.append(f)

                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

                return answer
            elif n == 4:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            for m in range(Number):
                                x1 = float(v[0][i])
                                x2 = float(v[1][j])
                                x3 = float(v[2][k])
                                x4 = float(v[3][m])
                                f = ne.evaluate(G)
                                fv.append(f)


                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

            elif n == 5:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            for m in range(Number):
                                for t in range(Number):
                                    x1 = float(v[0][i])
                                    x2 = float(v[1][j])
                                    x3 = float(v[2][k])
                                    x4 = float(v[3][m])
                                    x5 = float(v[4][t])
                                    f = ne.evaluate(G)
                                    fv.append(f)


                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

                return answer

            elif n == 6:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            for m in range(Number):
                                for t in range(Number):
                                    for g in range(Number):
                                        x1 = float(v[0][i])
                                        x2 = float(v[1][j])
                                        x3 = float(v[2][k])
                                        x4 = float(v[3][m])
                                        x5 = float(v[4][t])
                                        x6 = float(v[5][g])
                                        f = ne.evaluate(G)
                                        fv.append(f)


                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

                return answer

            elif n == 7:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            for m in range(Number):
                                for t in range(Number):
                                    for g in range(Number):
                                        for y in range(Number):
                                            x1 = float(v[0][i])
                                            x2 = float(v[1][j])
                                            x3 = float(v[2][k])
                                            x4 = float(v[3][m])
                                            x5 = float(v[4][t])
                                            x6 = float(v[5][g])
                                            x7 = float(v[6][y])
                                            f = ne.evaluate(G)
                                            fv.append(f)


                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

                return answer

            elif n == 8:
                fv = []
                for i in range(Number):
                    for j in range(Number):
                        for k in range(Number):
                            for m in range(Number):
                                for t in range(Number):
                                    for g in range(Number):
                                        for y in range(Number):
                                            for h in range(Number):
                                                x1 = float(v[0][i])
                                                x2 = float(v[1][j])
                                                x3 = float(v[2][k])
                                                x4 = float(v[3][m])
                                                x5 = float(v[4][t])
                                                x6 = float(v[5][g])
                                                x7 = float(v[6][y])
                                                x8 = float(v[7][h])
                                                f = ne.evaluate(G)
                                                fv.append(f)


                if len(answer) <= 1:
                    fmax = np.max(fv)
                    fmin = np.min(fv)
                    main = np.average(fv)
                    amt = .5 * (fmax-fmin)
                    answer.append(main)
                    answer.append(amt)
                    print(answer)

                return answer



        for Val in Vs[indx]:
            ls.append(Val)
            #print(ls)
            brute_force(ls, indx+1, total, Vs)
            ls=ls[0:indx]

    brute_force([],0,n,v)
    await ctx.send(f"The main value and uncertainty is {answer}. Don't you think I am wrong or something! >:C")

