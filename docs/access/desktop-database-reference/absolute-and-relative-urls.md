---
<<<<<<< Titre tête : absolue et Relative TOCTitle URL : ms:assetid URL absolues et relatives : 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea ms:mtpsurl : https://msdn.microsoft.com/library/JJ249501(v=office.15) ms:contentKeyID : ms.date 48545774 : mtps_version 18/09/2015 : v = Office.15
---

# <a name="absolute-and-relative-urls"></a>URL absolues et relatives

**S’applique à**: Access 2013 | Office 2013 

Une URL spécifie l'emplacement d'une cible sur un ordinateur local ou en réseau, par exemple un fichier, un répertoire, une page HTML, une image, un programme, etc *.* Dans cette présentation, une *URL absolue* a la forme suivante :
=======
titre : TOCTitle d’URL absolues et relatives : ms:assetid d’URL absolues et relatives : 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea ms:mtpsurl : https://msdn.microsoft.com/library/JJ249501(v=office.15) ms:contentKeyID : ms.date 48545774 : 17/10/2018 mtps_version : v=office.15
---

# <a name="absolute-and-relative-urls"></a>URL absolues et relatives

**S’applique à**: Access 2013 | Office 2013 

Une URL spécifie l’emplacement d’une cible sur un ordinateur local ou en réseau, telles qu’un fichier, répertoire, HTML page, image, programme et ainsi de suite. Dans cette discussion, une *URL absolue* est du formulaire :
>>>>>>> master

*modèle://serveur/chemin d'accès/ressource*

où :

<<<<<<< Tête
  - *modèle*

  - Spécifie comment la *ressource* est accessible.

  - *serveur*

  - Spécifie le nom de l’ordinateur où se trouve la *ressource* .

  - *chemin d'accès*

  - Indique la séquence de répertoires menant à la cible. Si la *ressource* est omise, la cible est le dernier répertoire figurant dans le *chemin d'accès*.

  - *ressource*

  - S’il est inclus, la *ressource* est la cible et est généralement le nom d’un fichier. Il peut être un *fichier simple* contenant un flux binaire d’octets ou un *document structuré,* contenant une ou plusieurs stockages et flux binaires d’octets.
=======
|Nom |Description|
|:----|:----------|
|*modèle*|Spécifie comment la *ressource* est accessible.|
|*serveur*|Spécifie le nom de l’ordinateur où se trouve la *ressource* .|
|*chemin d'accès*|Indique la séquence de répertoires menant à la cible. Si la *ressource* est omise, la cible est le dernier répertoire figurant dans le *chemin d'accès*.|
|*ressource*|S’il est inclus, la *ressource* est la cible et est généralement le nom d’un fichier. Il peut être un *fichier simple*contenant un flux binaire d’octets ou un *document structuré*contenant un ou plusieurs stockages et flux binaires d’octets.|
>>>>>>> master

Une *URL absolue* contient toutes les informations nécessaires pour localiser une ressource.

Une *URL relative* localise une ressource en utilisant une URL absolue comme point de départ. Dans la pratique, l' « URL complète » de la cible est spécifiée par la concaténation des URL absolue et relative. Une URL relative n'est constituée en général que du *chemin d'accès* et, éventuellement, de la *ressource*, mais pas du *modèle* ni du *serveur*.

<<<<<<< Tête
## <a name="url-scheme-registration"></a>Enregistrement du modèle d'URL

Si un fournisseur prend en charge plusieurs URL, il sera enregistré pour un ou plusieurs modèles d'URL. C'est-à-dire que les URL utilisant ces modèles appelleront automatiquement le fournisseur enregistré. Par exemple, le schéma *http* est enregistré pour le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). ADO suppose que toutes les URL avec le préfixe « http » représentent des dossiers ou fichiers Web à utiliser avec le fournisseur de publication Internet. Pour plus d'informations sur les modèles enregistrés par votre fournisseur, consultez la documentation de ce dernier.

## <a name="defining-context-with-a-url"></a>Définition d'un contexte avec une URL
=======
## <a name="url-scheme-registration"></a>Enregistrement du modèle d’URL

Si un fournisseur prend en charge plusieurs URL, il sera enregistré pour un ou plusieurs modèles d'URL. C'est-à-dire que les URL utilisant ces modèles appelleront automatiquement le fournisseur enregistré. Par exemple, le schéma *http* est enregistré pour le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). ADO suppose que toutes les URL, les préfixe « http » représentent des dossiers web ou fichiers à utiliser avec le fournisseur de publication Internet. Pour plus d'informations sur les modèles enregistrés par votre fournisseur, consultez la documentation de ce dernier.

## <a name="defining-context-with-a-url"></a>Définition d’un contexte avec une URL
>>>>>>> master

Une des fonctions d'une connexion ouverte, représentée par un objet [Connection](connection-object-ado.md), est de limiter les opérations ultérieures sur la source de données représentée par cette connexion. En d'autres termes, la connexion définit le contexte des opérations suivantes.

Avec ADO 2.5, une URL absolue peut également définir un contexte. Par exemple, lorsqu'un objet [Record](record-object-ado.md) est ouvert avec une URL absolue, un objet **Connection** est implicitement créé pour représenter la ressource spécifiée par l'URL.

<<<<<<< Tête d’une URL absolue qui définit un contexte peut être spécifiée dans le paramètre *ActiveConnection* de **l’enregistrement** de méthode [Open](open-method-ado-record.md) d’objet. Vous pouvez également spécifier une URL absolue comme valeur de la nouvelle « URL**=**« mot clé dans le paramètre *ConnectionString* méthode [Open](open-method-ado-connection.md) de **connexion** objet et la méthode [Open](open-method-ado-recordset.md) *ActiveConnection de l’objet [Recordset](recordset-object-ado.md) *paramètre.

Le contexte peut également être défini avec un objet **Record** ou **Recordset** ouvert qui représente un répertoire, car ces objets disposent déjà d'un objet **Connection** implicitement ou explicitement déclaré qui spécifie le contexte.

## <a name="scoped-operations"></a>Opérations de portée définie

Le contexte définit simultanément une *portée* — autrement dit, le répertoire et ses sous-répertoires pouvant participer aux opérations suivantes. L'objet **Record** comporte plusieurs méthodes de portée définie, notamment [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) et [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) qui s'appliquent à un répertoire et à ses sous-répertoires.

## <a name="relative-urls-as-command-text"></a>URL relatives sous la forme de texte de commande
=== Une URL absolue qui définit un contexte peut être spécifiée dans le paramètre *ActiveConnection* de la méthode [Open](open-method-ado-record.md) de l’objet **Record** . Vous pouvez également spécifier une URL absolue comme valeur de la nouvelle `URL=` mot clé dans le paramètre *ConnectionString* méthode [Open](open-method-ado-connection.md) de **connexion** objet et la méthode [Open](open-method-ado-recordset.md) *ActiveConnection* de l’objet [Recordset](recordset-object-ado.md) paramètre.

Le contexte peut également être défini avec un objet **Record** ou **Recordset** ouvert qui représente un répertoire, car ces objets disposent déjà d'un objet **Connection** implicitement ou explicitement déclaré qui spécifie le contexte.

## <a name="scoped-operations"></a>Opérations de portée définie

Le contexte définit simultanément une *portée*— autrement dit, le répertoire et ses sous-répertoires pouvant participer aux opérations suivantes. L'objet **Record** comporte plusieurs méthodes de portée définie, notamment [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) et [DeleteRecord](deleterecord-method-ado.md) qui s'appliquent à un répertoire et à ses sous-répertoires.

## <a name="relative-urls-as-command-text"></a>URL relatives sous forme de texte de commande
>>>>>>> master

Chaîne spécifiant une commande à exécuter sur la source de données peut être spécifiée dans le paramètre *CommandText* de méthode **Connection** objet **Execute** et le paramètre de la *Source* de méthode **Open** **Recordset** objet.

Une URL relative peut être spécifiée dans le paramètre *CommandText* ou *Source* . L'URL relative ne spécifie pas une commande (comme une commande SQL) ; elle est simplement spécifiée dans ces paramètres. En outre, le contexte de la connexion active doit être une URL absolue et le paramètre *Option* doit être défini **adCmdTableDirect**.

Par exemple, un objet **Recordset** peut être ouvert sur le fichier Readme25.txt du répertoire Winnt/system32 comme suit :

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< HEAD l’URL absolue dans la chaîne de connexion spécifie le serveur (YourServer) et le chemin d’accès () et le chemin d’accès (Winnt). Cette URL définit également le contexte.

L’URL relative dans le texte de commande utilise l’URL absolue comme point de départ et spécifie le reste du chemin d’accès (system32) et le fichier à ouvrir () et le fichier à ouvrir (Readme25.txt).

<a name="the-options-field--indicates-that-the-command-type-is-a-relative-url"></a>Le champ d’options () indique que le type de commande est une URL relative.
=======
L’URL absolue dans la chaîne de connexion spécifie le serveur (YourServer) et le chemin d’accès (Winnt). Cette URL définit également le contexte.

L’URL relative dans le texte de commande utilise l’URL absolue comme point de départ et spécifie le reste du chemin d’accès (system32) et le fichier à ouvrir (Readme25.txt).

Le champ d’options indique que le type de commande est une URL relative.
>>>>>>> master

Autre exemple, le code suivant ouvre un **objet Recordset** sur le contenu du répertoire :

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< Tête
## <a name="ole-db-provider-supplied-url-schemes"></a>Modèles d'URL fournis par le fournisseur OLE DB

La première partie d’une URL complète est le *schéma* utilisé pour accéder à la ressource identifiée par le reste de l’URL. Par exemple, HTTP (HyperText Transfer Protocol) et FTP (File Transfer Protocol).

<a name="ado-supports-ole-db-providers-that-recognize-their-own-url-schemes-for-example-the-microsoft-ole-db-provider-for-internet-publishingmicrosoft-ole-db-provider-for-internet-publishingmd-which-accesses-published-windows-2000-files-recognizes-the-existing-http-scheme"></a>ADO prend en charge les fournisseurs OLE DB qui reconnaissent leurs propres schémas d’URL. Par exemple, le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)*,* qui accède aux fichiers Windows 2000 « publiés », reconnaît le modèle HTTP existant.
=======
## <a name="ole-db-provider-supplied-url-schemes"></a>Modèles d’URL fournis par le fournisseur OLE DB

La première partie d’une URL complète est le *schéma* utilisé pour accéder à la ressource identifiée par le reste de l’URL. Par exemple, HTTP (HyperText Transfer Protocol) et FTP (File Transfer Protocol).

ADO prend en charge les fournisseurs OLE DB qui reconnaissent leurs propres schémas d’URL. Par exemple, le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), qui accède aux fichiers Windows 2000 « publiés », reconnaît le modèle HTTP existant.
>>>>>>> master

