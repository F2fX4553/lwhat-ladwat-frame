# lwhat-ladwat-frame
def bgall(pos,bg):
    pos.update()
    clt = pos.winfo_children()
    pos.config(bg=bg)
    my = ttk.Style()
    my.configure('TRadiobutton', background=bg)
    my.configure('TCheckbutton', background=bg)
    for c in clt:
        if c.winfo_class() == 'Frame': bgall(c,bg)
        try:
            c ['bg']=bg
        except:
            pass
        try:
            c ['background']= bg
        except:
            pass

def fgall(pos,fg):
    pos.update()
    clt = pos.winfo_children()
    my = ttk.Style()
    my.configure('TButton', foreground=fg)
    my.configure('TRadiobutton', foreground=fg)
    my.configure('TTCheckbutton', foreground=fg)
    for c in clt:
        if c.winfo_class() == 'Frame': fgall(c,fg)
        try:
            c['foreground']= fg
        except:
            pass



def fontall(pos,font):
    pos.update()
    clt = pos.winfo_children()
    my = ttk.Style()
    my.configure('TButton', font=font)
    my.configure('TRadiobutton', font=font)
    my.configure('TCheckbutton', font=font)
    for c in clt:
        if c.winfo_class() == 'Frame': fontall(c,font)
        try:
            c['font']= font
        except:
            pass
