---
title: Analyse de l’historique de téléchargement de message pour un compte POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: Cette rubrique décrit la structure du BLOB POP3 qui représente l'historique de téléchargement des messages d'un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés de ce compte.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327760"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analyse de l’historique de téléchargement de message pour un compte POP3

Cette rubrique décrit la structure du BLOB POP3 qui représente l'historique de téléchargement des messages d'un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés de ce compte.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Pourquoi analyser l'historique de téléchargement des messages?

Le fournisseur POP (Post Office Protocol) pour Outlook permet aux utilisateurs de récupérer et de télécharger de nouveaux messages électroniques sur leur appareil local, puis de laisser ou de supprimer ces messages électroniques sur le serveur de messagerie. Lorsque le client de messagerie recherche les nouveaux messages à télécharger, il doit être en mesure d'identifier et de télécharger uniquement les nouveaux messages pour cette boîte de réception. Le client de messagerie effectue cette opération en utilisant d'abord la commande UIDL (ID unique) pour obtenir une carte de chaque message qui a déjà été remis à la boîte de réception à un identificateur unique (UID). Le client obtient également l'historique de téléchargement des messages pour les messages qui ont été téléchargés ou supprimés pour la boîte de réception sur ce client. À l'aide de la carte UID de message et de l'historique de téléchargement, le client peut ensuite identifier les messages qui ne sont pas présents dans l'historique comme étant nouveaux et, par conséquent, doit être téléchargé.
  
Pour obtenir l'historique de téléchargement des messages pour une boîte de réception:
  
- Suivez les étapes de la [recherche de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md) afin de trouver la propriété [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , qui contient un objet BLOB (Binary Large Object) qui représente l'historique des messages pour un compte POP3. 
    
- Lisez cette rubrique, qui décrit la structure du BLOB, et montre un exemple d'objet BLOB pour identifier les messages qui ont été téléchargés ou supprimés pour la boîte de réception du compte POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Structure BLOB de POP

La structure de l'objet BLOB POP, comme décrit dans le tableau 1, commence par deux champs, **version** et **Count**, suivi par un nombre de balises de ressource, chacune étant terminée par un caractère null. **** 
  
**Tableau 1. Structure du BLOB qui représente l'historique de téléchargement des messages d'un compte POP3**

|**Champ dans l'objet BLOB**|**Size**|**Description**|
|:-----|:-----|:-----|
|**Version** <br/> |2 octets  <br/> |Doit être 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 octets  <br/> |Nombre de balises de ressource dans cet objet BLOB.  <br/> |
|Balise de ressource  <br/> |Variable  <br/> |0 ou plusieurs chaînes UTF-8 se terminant par null qui codent les balises de la ressource. Le nombre de chaînes terminées par un caractère null **** doit correspondre au nombre.  <br/> |
   
Chaque balise de ressource spécifie l'opération appliquée à un message, les métadonnées de date et d'heure relatives à l'opération et encode l'UID du message. Le format d'une chaîne de balise de ressource est décomposé comme suit, et est expliqué en détail dans le tableau 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tableau 2. Structure d'une balise de ressource**

|**Champ dans une balise de ressource**|**Size**|**Description**|
|:-----|:-----|:-----|
| `O` <br/> |1 caractère  <br/> |Opération effectuée sur le message électronique. La valeur doit être «+», «-» ou «&amp;», ce qui indique respectivement une opération Get, Delete ou Get-and-Delete réussie.  <br/> |
| `c` <br/> |1 caractère  <br/> |Partie du contenu du message impliqué dans l'opération. La valeur doit être «», «h» ou «b», qui indique respectivement le contenu de l'élément None, Header ou Body.  <br/> |
| `yyyy` <br/> |4 caractères  <br/> |Année à quatre chiffres de l'opération.  <br/> |
| `MM` <br/> |2 caractères  <br/> |Mois de l'opération à deux chiffres.  <br/> |
| `dd` <br/> |2 caractères  <br/> |Jour de l'opération à deux chiffres.  <br/> |
| `hh` <br/> |2 caractères  <br/> |Heure de l'opération à deux chiffres.  <br/> |
| `mm` <br/> |2 caractères  <br/> |Minute de l'opération à deux chiffres.  <br/> |
| `ss` <br/> |2 caractères  <br/> |Seconde de l'opération à deux chiffres.  <br/> |
| `uuu…` <br/> |Longueur variable  <br/> |UID codée d'un message.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Exemple

La figure 1 montre un exemple d'objet BLOB qui représente l'historique de téléchargement des messages d'un compte POP. 
  
**Figure 1. Exemple de structure BLOB pour l'historique de téléchargement des messages d'un compte POP3**

![BLOB de l’historique de téléchargement des messages d’un compte POP3](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
En fonction de la structure décrite dans le tableau 1 et le tableau 2, cet objet BLOB représente l'historique de téléchargement de 23 messages électroniques.
  
Pour analyser l'UID brute dans chaque balise de ressource, sachez que l'UID suit ce codage: les caractères d'un UID sont essentiellement des caractères alphanumériques et chaque caractère non alphanumérique est précédé du caractère ASCII «$» (0x24). Par conséquent, les caractères ASCII $2D représentent le caractère non alphanumérique «-». La figure 2 montre un exemple de première conversion de l'UID brut dans la balise de ressource 1 en une représentation ASCII, puis la conversion de tout caractère non alphanumérique précédé de «$» pour produire l'UID réel:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Figure 2. Conversion de l'UID brut dans une balise de ressource en un UID de message réel**

![Conversion d’un UID brut dans BLOB vers l’UID de message actuel](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Pour interpréter la balise de ressource 1 dans cet objet BLOB: le `0BC535DB-EA63-11E1-A75C-00215AD7BB74` message avec l'UID a été récupéré avec succès le 6 septembre 2012, à 13:11:38. 
  
Vous pouvez également analyser les 22 balises de ressource restantes pour ce BLOB.
  
## <a name="see-also"></a>Voir aussi
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analyse de l'historique de la commande UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

