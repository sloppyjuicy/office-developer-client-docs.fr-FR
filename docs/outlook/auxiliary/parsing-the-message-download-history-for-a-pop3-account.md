---
title: Analyse de l’historique de téléchargement de message pour un compte POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: Cette rubrique décrit la structure du BLOB POP3 qui représente l’historique de téléchargement des messages d’un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés sur ce compte.
ms.openlocfilehash: e2b4f3e94b187bbae137cf833c5e68604309d19d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776668"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analyse de l’historique de téléchargement de message pour un compte POP3

Cette rubrique décrit la structure du BLOB POP3 qui représente l’historique de téléchargement des messages d’un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés sur ce compte.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Pourquoi l’historique de téléchargement des messages ?

Le fournisseur POP (Post Office Protocol) pour Outlook permet aux utilisateurs de récupérer et de télécharger de nouveaux messages électroniques sur leur appareil local, puis de les laisser ou de les supprimer sur le serveur de messagerie. Lorsque le client de messagerie recherche les nouveaux messages à télécharger, il doit être en mesure d’identifier et de télécharger uniquement les nouveaux messages pour cette boîte de réception. Pour ce faire, le client de messagerie utilise d’abord la commande UIDL (Unique ID Listing) pour obtenir une carte de chaque message qui a déjà été remis à cette boîte de réception à un identificateur unique (UID). Le client obtient également l’historique de téléchargement des messages pour les messages qui ont été téléchargés ou supprimés pour la boîte de réception sur ce client. À l’aide de la carte UID du message et de l’historique de téléchargement, le client peut ensuite identifier les messages absents de l’historique comme nouveaux et, par conséquent, doivent être téléchargés.
  
Pour obtenir l’historique de téléchargement des messages pour une boîte de réception :
  
- Suivez les étapes de recherche de l’historique de téléchargement des messages pour un compte [POP3](locating-the-message-download-history-for-a-pop3-account.md) pour rechercher la propriété [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , qui contient un objet BLOB (Binary Large Object) qui représente l’historique des messages d’un compte POP3. 
    
- Lisez cette rubrique, qui décrit la structure du BLOB et présente un exemple blob pour identifier les messages qui ont été téléchargés ou supprimés pour la boîte de réception du compte POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Structure BLOB POP

La structure BLOB POP, comme décrit dans le tableau 1, commence par deux champs, **Version** et **Count**, suivis d’un nombre de balises de ressources, chacune étant terminée par null. 
  
**Tableau 1. Structure du BLOB qui représente l’historique de téléchargement des messages d’un compte POP3**

|**Champ dans BLOB**|**Taille**|**Description**|
|:-----|:-----|:-----|
|**Version** <br/> |2 octets  <br/> |Doit être 3 (**PBLOB_VERSION_NUM**). |
|**Count** <br/> |2 octets  <br/> |Nombre de balises de ressource dans cet objet BLOB. |
|Balise de ressource  <br/> |Variable  <br/> |0 ou plus chaînes UTF-8 terminées par null qui encodent les balises de ressource. Le nombre de chaînes terminées par null doit correspondre à **Nombre**. |
   
Chaque balise de ressource spécifie l’opération qui est appliquée à un message, certaines métadonnées date-heure sur l’opération et code l’UID du message. Le format d’une chaîne de balise de ressource est décomposé comme suit et est expliqué plus en détail dans le tableau 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tableau 2. Structure d’une balise de ressource**

|**Champ dans une balise de ressource**|**Taille**|**Description**|
|:-----|:-----|:-----|
| `O` <br/> |1 caractère  <br/> |Opération effectuée sur le message électronique. La valeur doit être « + », « - » ou « »,&amp; ce qui indique une opération get, delete ou get-and-delete réussie, respectivement. |
| `c` <br/> |1 caractère  <br/> |Partie du contenu du message impliquée dans l’opération. La valeur doit être « « , « h » ou « b », ce qui indique le contenu d’aucun, d’en-tête ou de corps, respectivement. |
| `yyyy` <br/> |4 caractères  <br/> |Année à quatre chiffres de l’opération. |
| `MM` <br/> |2 caractères  <br/> |Mois à deux chiffres de l’opération. |
| `dd` <br/> |2 caractères  <br/> |Jour à deux chiffres de l’opération. |
| `hh` <br/> |2 caractères  <br/> |Heure à deux chiffres de l’opération. |
| `mm` <br/> |2 caractères  <br/> |Minute à deux chiffres de l’opération. |
| `ss` <br/> |2 caractères  <br/> |Seconde à deux chiffres de l’opération. |
| `uuu…` <br/> |Longueur variable  <br/> |UID codé d’un message. |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Exemple

La figure 1 montre un exemple d’objet BLOB qui représente l’historique de téléchargement des messages d’un compte POP. 
  
**Figure 1. Exemple de structure BLOB pour l’historique de téléchargement des messages d’un compte POP3**

![BLOB de l’historique de téléchargement des messages d’un compte POP3](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
En fonction de la structure décrite dans les tableaux 1 et 2, ce BLOB représente l’historique de téléchargement de 23 messages électroniques.
  
Pour identifier l’UID brut dans chaque balise de ressource, n’ignorez pas que l’UID suit ce codage : les caractères d’un UID sont principalement des caractères alphanumériques et chaque caractère non alphanumérique est précédé du caractère ASCII « $ » (0x24). Ainsi, les caractères ASCII $2d représentent le caractère non alphanumérique « - ». La figure 2 montre un exemple de conversion de l’UID brut dans la balise de ressource 1 en représentation ASCII, puis de tout caractère non alphanumérique précédé de « $ » pour produire l’UID réel :
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Figure 2. Conversion de l’UID brut dans une balise de ressource en UID de message réel**

![Conversion d’un UID brut dans BLOB vers l’UID de message actuel](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Pour interpréter la balise de ressource 1 dans ce BLOB : le message avec l’UID  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` a été récupéré avec succès le 6 septembre 2012 à 13:11:38. 
  
Vous pouvez de même, pour ce BLOB, l’une des 22 balises de ressources restantes.
  
## <a name="see-also"></a>Voir aussi
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Parsage de l’historique UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

