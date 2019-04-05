---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Ajouter un enregistrement de zone DNS
{:#add-a-dns-zone-record}

Après avoir [ajouté une zone DNS](/docs/infrastructure/dns?topic=dns-add-a-dns-zone), vous pouvez ajouter des enregistrements à la zone à tout moment. Ces enregistrements incluent :

* Enregistrements A (Hôte)
* Enregistrements AAAA (Hôte)
* Enregistrements CNAME (Alias)
* Enregistrements MX (Echange de courrier)
* Enregistrements TXT (Texte)
* Enregistrements SRV (Service)

Effectuez les étapes ci-dessous pour ajouter un enregistrement de zone DNS.

* Accédez à l'écran de la **zone DNS** souhaitée. Reportez-vous à la section [Utilisation de l'écran de zones DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens).
* Sélectionnez la zone DNS à laquelle l'enregistrement sera ajouté.
* Sélectionnez le **type de ressource** souhaité dans la liste déroulante **Type de ressource**.
* Remplissez les champs restants du nouvel enregistrement. Pour plus d'informations, référez-vous au tableau ci-dessous :<br/><br/><table border="1"><tbody><tr><th scope="col">Type d'enregistrement</th><th scope="col">Champ</th><th scope="col">Entrée</th></tr><tr><td rowspan="3">A (Hôte), AAAA (Hôte) ou CNAME (Alias)</td><td>Hôte</td><td>Entrez le <strong>nom d'hôte</strong>.</td></tr><tr><td>Pointe vers</td><td>Entrez l'<strong>adresse IP</strong> vers laquelle pointe l'enregistrement hôte.</td></tr><tr><td>Durée de vie</td><td>Sélectionnez la durée de vie (TTL) dans la liste déroulante. La valeur par défaut de TTL est 15 minutes.</td></tr><tr><td rowspan="4">MX (Echange de courrier)</td><td>Priorité</td><td>Entrez la <strong>priorité</strong> de l'hôte cible. Plus la valeur est faible, plus la priorité est élevée.</td></tr><tr><td>Hôte</td><td>Entrez le <strong>nom d'hôte</strong>.</td></tr><tr><td>Va</td><td>Entrez le <strong>CNAME</strong> du serveur de messagerie. Ceci est généralement représenté par mail.example.com.</td></tr><tr><td>Durée de vie</td><td>Sélectionnez la durée de vie (TTL) dans la liste déroulante. La valeur par défaut de TTL est 15 minutes.</td></tr><tr><td rowspan="3">TXT (Texte)</td><td>Nom</td><td>Entrez le signe <strong>@</strong> ou le <strong>nom de domaine</strong>.</td></tr><tr><td>Valeur</td><td>Entrez l'<strong>enregistrement</strong> pour vérifier les droits de fin de courrier électronique appropriés pour un domaine ou une adresse IP.</td></tr><tr><td>Durée de vie</td><td>Sélectionnez la durée de vie (TTL) dans la liste déroulante. La valeur par défaut de TTL est 15 minutes.</td></tr><tr><td rowspan="8">SRV (Enregistrement de service)</td><td>Service</td><td>Entrez le <strong>nom symbolique</strong> du service souhaité.</td></tr><tr><td>Protocole</td><td>Sélectionnez le <strong>protocole</strong> utilisé dans la liste déroulante.</td></tr><tr><td>Priorité</td><td>Entrez la <strong>priorité</strong> de l'hôte cible. Plus la valeur est faible, plus la priorité est élevée.</td></tr><tr><td>Poids</td><td>Entrez le <strong>poids relatif</strong> pour les enregistrements ayant la même priorité.</td></tr><tr><td>Port</td><td>Entrez le <strong>port TCP ou UPD</strong> sur lequel le service doit être trouvé.</td></tr><tr><td>Hôte (facultatif)</td><td>Entrez le <strong>nom d'hôte</strong> du service.</td></tr><tr><td>Cible</td><td>Entrez le <strong>nom d'hôte canonique de la machine</strong> fournissant le service.</td></tr><tr><td>Durée de vie</td><td>Sélectionnez la durée de vie (TTL) dans la liste déroulante. La valeur par défaut de TTL est 15 minutes.</td></tr></tbody></table><br/>
* Sélectionnez le bouton **Ajouter enregistrement** pour ajouter le nouvel enregistrement de zone.

## Etapes suivantes
{:#add-a-dns-zone-record-next}

Lorsque vous ajoutez l'enregistrement de zone, il apparaît dans la section **Enregistrements existants** de l'écran. Vous pouvez [modifier](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) ou [supprimer](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) l'enregistrement de zone à tout moment.
