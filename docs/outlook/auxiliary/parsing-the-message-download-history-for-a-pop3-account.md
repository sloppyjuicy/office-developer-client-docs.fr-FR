---
title: Analyse de l’historique de téléchargement de message pour un compte POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: Cette rubrique décrit la structure de l’objet BLOB POP3 qui représente l’historique de téléchargement des messages d’un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés sur ce compte.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389007"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analyse de l’historique de téléchargement de message pour un compte POP3

Cette rubrique décrit la structure de l’objet BLOB POP3 qui représente l’historique de téléchargement des messages d’un compte POP3, pour identifier les messages qui ont été téléchargés ou supprimés sur ce compte.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Pourquoi analyser l’historique de téléchargement des messages ?

Le fournisseur Post Office Protocol (POP) pour Outlook permet aux utilisateurs pour récupérer et télécharger les nouveaux messages électroniques sur leur appareil local et ensuite conserver ou supprimer les messages électroniques sur le serveur de messagerie. Lorsque le client de messagerie vérifie les nouveaux messages à télécharger, il doit être en mesure d’identifier et de télécharger uniquement les nouveaux messages pour cette boîte de réception. Pour cela, le client de messagerie premier à l’aide de la commande UIDL (liste des ID uniques) pour obtenir un mappage de chaque message qui a déjà été remis à cette boîte de réception à un identificateur unique (UID). Le client obtient également l’historique de téléchargement du message pour les messages qui ont été téléchargés ou supprimés de la boîte de réception sur ce client. À l’aide de la carte UID de message et l’historique de téléchargement, le client peut ensuite identifier les messages qui sont absents de l’historique en tant que nouvelle et, par conséquent, doit être téléchargé.
  
Pour obtenir les messages d’historique de téléchargement pour une boîte de réception :
  
- Suivez les étapes de [localiser le message l’historique d’un compte POP3 de téléchargement](locating-the-message-download-history-for-a-pop3-account.md) pour trouver la propriété [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , qui contient un grand BLOB (binary object) qui représente l’historique des conversations d’un compte POP3. 
    
- Lisez cette rubrique, qui décrit la structure de l’objet BLOB et montre un exemple BLOB pour identifier les messages qui ont été téléchargés ou supprimés de la boîte de réception du compte POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Structure BLOB POP

La structure des objets BLOB POP, comme décrit dans le tableau 1, commence par deux champs, **Version** et **Count**, suivi **d’un nombre de balises de ressources, chacun d'entre eux est terminée** . 
  
**Le tableau 1. Structure de l’objet BLOB qui représente le message d’historique de téléchargement d’un compte POP3**

|**Champ BLOB**|**Taille**|**Description**|
|:-----|:-----|:-----|
|**Version** <br/> |2 octets  <br/> |Doit être 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 octets  <br/> |Le nombre de balises de ressource dans cet BLOB.  <br/> |
|Balise de ressource  <br/> |Variable  <br/> |0 ou plus nul chaînes UTF-8 coder les balises de ressources. Le nombre de chaînes doit correspondre à **Count**.  <br/> |
   
Chaque ressource spécifie l’opération qui est appliquée à un message, des métadonnées de date-heure sur l’opération et le code de l’UID du message. Le format d’une chaîne de balise de ressource se décompose comme suit et est expliqué dans le tableau 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Le tableau 2. Structure d’une balise de ressource**

|**Champ dans une balise de ressource**|**Taille**|**Description**|
|:-----|:-----|:-----|
| `O` <br/> |1 caractère  <br/> |L’opération effectuée sur le message électronique. La valeur doit être « + », «- », ou «&amp;», qui indique une réussite get, supprimer ou opération get-delete, respectivement.  <br/> |
| `c` <br/> |1 caractère  <br/> |La partie du contenu du message impliqué dans l’opération. La valeur doit être « », « h » ou « b », qui indique le contenu None, en-tête ou corps, respectivement.  <br/> |
| `yyyy` <br/> |4 caractères  <br/> |Année à quatre chiffres de l’opération.  <br/> |
| `MM` <br/> |2 caractères  <br/> |Le deux chiffres du mois de l’opération.  <br/> |
| `dd` <br/> |2 caractères  <br/> |Jour de l’opération à deux chiffres.  <br/> |
| `hh` <br/> |2 caractères  <br/> |L’heure à deux chiffres de l’opération.  <br/> |
| `mm` <br/> |2 caractères  <br/> |La minute à deux chiffres de l’opération.  <br/> |
| `ss` <br/> |2 caractères  <br/> |La seconde à deux chiffres de l’opération.  <br/> |
| `uuu…` <br/> |Longueur variable  <br/> |L’UID codé d’un message.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Exemple

La figure 1 montre un exemple d’un objet BLOB qui représente l’historique de téléchargement des messages d’un compte POP. 
  
**La figure 1. Exemple de structure de BLOB pour le message d’historique de téléchargement d’un compte POP3**

![BLOB de l’historique de téléchargement des messages d’un compte POP3](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
En fonction de la structure décrite dans le tableau 1 et 2 du tableau, cet objet BLOB représente l’historique de téléchargement des messages électroniques 23.
  
Pour analyser l’UID brut dans chaque balise ressources, sachez que l’UID suit ce codage : caractères dans un UID sont principalement des caractères alphanumériques, et chaque caractère non alphanumérique est précédé du caractère ASCII « $» (0 x 24). Afin que les caractères ASCII $2d représentent la non alphanumériques caractère «- ». La figure 2 illustre un exemple de conversion tout d’abord l’UID brut dans la balise de ressource 1 à la représentation ASCII, puis convertir n’importe quel caractère non alphanumérique, précédé de « $» pour générer l’UID réel :
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**La figure 2. Conversion de l’UID brut dans une balise de ressources vers l’UID de message**

![Conversion d’un UID brut dans BLOB vers l’UID de message actuel](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Pour interpréter la balise de ressource 1 dans ce BLOB : le message avec l’UID `0BC535DB-EA63-11E1-A75C-00215AD7BB74` a été récupéré correctement sur 6 septembre 2012, à 13:11:38. 
  
Vous pouvez même analyser les balises restantes de la 22 ressource pour ce BLOB.
  
## <a name="see-also"></a>Voir aussi
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [L’analyse de l’historique UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

