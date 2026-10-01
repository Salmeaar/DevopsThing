## terrafrom infran

1.Först lagade jag autentiseringen i cPouta och sedan ändrade jag värden i terraform.tfvars

2.Sedan körde jag kommandon för att checka att filen skulle vara conffad rätt(den var inte). Varefter jag körde med terraform apply

![Bild av den lyckade apply:n](./m8-bilder/succeeded-tf-apply.png)

3.När jag sedan körde curl:en kom det problem d jag hade fyllt confen fel och hade stora bokstäver men efter fixen fick jag rätt

![Bevis på lyckade curlen](./m8-bilder/funkande-curlen.png)

4.Steg 6 -> efter det rev jag ner den manuella VM:n

![Bevis på Instansen](./m8-bilder/instances-post-delete.png)
![Bevis på floating IP](./m8-bilder/floatingIP-post-delete.png)

Sedan checkade jag terraforms statelist
![Bild på state listen](./m8-bilder/terraform-state-list.png)

5.Steg 8 -> jag testade terraform output floating-ip, destroya den, applya pånytt o desta samma kommando pånytt
![Bild på båda outputten](./m8-bilder/före-och-efter-destroyApply.png)