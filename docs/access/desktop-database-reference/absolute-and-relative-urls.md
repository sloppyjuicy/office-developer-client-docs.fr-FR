---
title: URL absolues et relatives
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282100"
---
# <a name="absolute-and-relative-urls"></a>URL absolues et relatives

**S’applique à** : Access 2013, Office 2013    

Une URL spécifie l'emplacement d'une cible sur un ordinateur local ou en réseau, par exemple un fichier, un répertoire, une page HTML, une image, un programme, etc. Dans cette présentation, une *URL absolue* a la forme suivante :

*modèle://serveur/chemin d'accès/ressource*

où :

|Nom |Description|
|:----|:----------|
|*modèle*|Indique comment accéder à la *ressource*.|
|*Serveur*|Indique le nom de l'ordinateur où réside la *ressource*.|
|*chemin d'accès*|Indique la séquence de répertoires menant à la cible. Si la *ressource* est omise, la cible est le dernier répertoire figurant dans le *chemin d'accès*.|
|*resource*|Si elle est incluse, la *ressource* est la cible et indique en général le nom d'un fichier. Il peut s’agit d’un *fichier simple* contenant un seul flux binaire d’octets ou d’un *document* structuré contenant un ou plusieurs stockages et des flux binaires d’octets.|

Une *URL absolue* contient toutes les informations nécessaires pour localiser une ressource.

Une *URL relative* localise une ressource en utilisant une URL absolue comme point de départ. Dans la pratique, l' « URL complète » de la cible est spécifiée par la concaténation des URL absolue et relative. Une URL relative n'est constituée en général que du *chemin d'accès* et, éventuellement, de la *ressource*, mais pas du *modèle* ni du *serveur*.

## <a name="url-scheme-registration"></a>Enregistrement du schéma d’URL

Si un fournisseur prend en charge plusieurs URL, il sera enregistré pour un ou plusieurs modèles d'URL. C'est-à-dire que les URL utilisant ces modèles appelleront automatiquement le fournisseur enregistré. Par exemple, le modèle *http* est enregistré pour le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). ADO suppose que toutes les URL préfixées avec le préfixe « http » représentent des dossiers web ou des fichiers à utiliser avec le fournisseur de publication Internet. Pour plus d'informations sur les modèles enregistrés par votre fournisseur, consultez la documentation de ce dernier.

## <a name="defining-context-with-a-url"></a>Définition d’un contexte avec une URL

Une des fonctions d'une connexion ouverte, représentée par un objet [Connection](connection-object-ado.md), est de limiter les opérations ultérieures sur la source de données représentée par cette connexion. En d'autres termes, la connexion définit le contexte des opérations suivantes.

Avec ADO 2.5, une URL absolue peut également définir un contexte. Par exemple, lorsqu'un objet [Record](record-object-ado.md) est ouvert avec une URL absolue, un objet **Connection** est implicitement créé pour représenter la ressource spécifiée par l'URL.

Une URL absolue qui définit un contexte peut être spécifiée dans le nouveau paramètre *ActiveConnection* de la méthode [Open](open-method-ado-record.md) de l'objet **Record**. Une URL absolue peut également être spécifiée en tant que valeur du nouveau mot clé dans le paramètre `URL=` *ConnectionString* de la méthode [Open](open-method-ado-connection.md) de l’objet **Connection** et du paramètre *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) de l’objet [Recordset.](recordset-object-ado.md)

Le contexte peut également être défini avec un objet **Record** ou **Recordset** ouvert qui représente un répertoire, car ces objets disposent déjà d'un objet **Connection** implicitement ou explicitement déclaré qui spécifie le contexte.

## <a name="scoped-operations"></a>Opérations limitées

Le contexte définit simultanément une *étendue,* c’est-à-dire le répertoire et ses sous-répertoires qui peuvent participer aux opérations suivantes. L'objet **Record** comporte plusieurs méthodes de portée définie, notamment [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) et [DeleteRecord](deleterecord-method-ado.md) qui s'appliquent à un répertoire et à ses sous-répertoires.

## <a name="relative-urls-as-command-text"></a>URL relatives en tant que texte de commande

Il est possible de spécifier une commande à exécuter sur la source de données dans le paramètre *CommandText* de la méthode **Execute** de l'objet **Connection** et le paramètre *Source* de la méthode **Open** de l'objet **Recordset**.

Il est également possible de spécifier une URL relative dans le paramètre *CommandText* ou *Source*. L'URL relative ne spécifie pas une commande (comme une commande SQL) ; elle est simplement spécifiée dans ces paramètres. En outre, le contexte de la connexion active doit être une URL absolue et le paramètre *Option* doit avoir la valeur **adCmdTableDirect**.

Par exemple, un objet **Recordset** peut être ouvert sur le fichier Readme25.txt du répertoire Winnt/system32 comme suit :

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

L’URL absolue dans la chaîne de connexion spécifie le serveur (YourServer) et le chemin d’accès (Winnt). Cette URL définit également le contexte.

L’URL relative dans le texte de commande utilise l’URL absolue comme point de départ et spécifie le reste du chemin d’accès (system32) et le fichier à ouvrir (Readme25.txt).

Le champ Options indique que le type de commande est une URL relative.

Autre exemple : le code suivant ouvre un **recordset** sur le contenu du répertoire :

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>Schémas d’URL fournis par le fournisseur OLE DB

Le début d'une URL complète est le *modèle* utilisé pour accéder à la ressource identifiée par le reste de l'URL. Par exemple, HTTP (HyperText Transfer Protocol) et FTP (File Transfer Protocol).

ADO supports OLE DB providers that recognize their own URL schemes. Par exemple, le fournisseur [Microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)pour la publication Internet, qui accède aux fichiers « publiés » Windows 2000, reconnaît le schéma HTTP existant.

