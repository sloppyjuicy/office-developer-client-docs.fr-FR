---
title: À propos des URL MAPI pour l’indexation Notification-Based
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: Cet article fournit une description détaillée des URL MAPI pour l’indexation basée sur les notifications.
ms.openlocfilehash: d6ce6145f82a54952d9217cd7fe330f99c817d8d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817577"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>À propos des URL MAPI pour l’indexation Notification-Based

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un fournisseur de magasin avertit un indexeur qu’un objet est prêt pour l’indexation, il génère une URL MAPI qui identifie de façon unique l’objet au gestionnaire de protocole MAPI. Les URL MAPI sont encodées dans Unicode et ont le format suivant : 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

Le tableau suivant décrit les différentes parties d’une URL classique.

|Élément | Description|
|:----|:-----------|  
|*SID* |Identificateur de sécurité de l’utilisateur actuel.| 
|*StoreDisplayName* |Chaîne qui spécifie le nom d’affichage de l’utilisateur sur ce magasin.|
|*HashNumber* |**DWORD** dans une représentation hexadécimale calculée en fonction de l’ID d’entrée de magasin ou de la signature de mappage de magasin. Cette valeur est stockée dans le Registre et sera utilisée ultérieurement pour identifier le magasin dans le gestionnaire de protocole MAPI.<br/><br/>Ce nombre doit être calculé de manière à réduire les collisions avec d’autres magasins. Pour l’algorithme que Microsoft Outlook utilise pour calculer le numéro de hachage, consultez [l’algorithme pour calculer le numéro de hachage du Magasin](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Nombre qui identifie le type du magasin qui contient l’objet à indexer. Les valeurs possibles sont les suivantes :<br/>- 0 - Magasin par défaut.<br/><br/>- 1 - Magasin délégué, utilisé pour les éléments délégués mis en cache localement.<br/><br/>- 2 - Dossiers publics, utilisés pour les favoris des dossiers publics.<br/><br/>**REMARQUE** : si le magasin est analysé au lieu d’être poussé, la valeur utilisée est le caractère *X*.| 
|*FolderNameA/.../FolderNameN* |Chemin d’accès de la racine de l’IPM_SUBTREE au dossier ou au message. Par exemple, un message dans le dossier **Famille** sous **Boîte de réception** contient **la boîte de réception/la famille** pour ce paramètre. |
|*EntryIDEncoded* |ID d’entrée MAPI pour l’élément encodé sous forme de chaîne Unicode. Consultez la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont encodés. Pour plus d’informations sur l’algorithme permettant d’encoder l’ID d’entrée, consultez [Algorithme pour encoder les ID d’entrée et les ID de pièce jointe](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**REMARQUE** : Lorsqu’il est affiché sous forme de texte, cet ID d’entrée encodé apparaît sous forme de caractères hangûl aléatoires ou de zones conformes à l’algorithme, en fonction des polices disponibles.  |
|*AttachIDEncoded* |ID de pièce jointe encodé sous la forme d’une chaîne Unicode. Consultez la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont encodés. Pour plus d’informations sur l’algorithme permettant d’encoder l’ID d’entrée, consultez [Algorithme pour encoder les ID d’entrée et les ID de pièce jointe](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**REMARQUE** : Lorsqu’il est affiché sous forme de texte, cet ID d’entrée encodé apparaît sous forme de caractères hangûl aléatoires ou de zones conformes à l’algorithme, en fonction des polices disponibles. |
|*FileName* |Nom du fichier pièce jointe, tel qu’il apparaît dans le message.|
    
## <a name="examples-of-mapi-urls"></a>Exemples d’URL MAPI

Voici quelques exemples d’URL MAPI.
  
- URL MAPI pour un dossier : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL MAPI pour un message : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL MAPI pour une pièce jointe : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caractères spéciaux

Certains caractères sont encodés s’ils apparaissent dans le message ou la pièce jointe. Les éléments suivants indiquent quels caractères sont encodés dans une URL MAPI :
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Objet blob associé à chaque URL MAPI

Lors de l’envoi (push) d’une URL MAPI pour un objet à indexer, un fournisseur de magasin crée également un objet blob (binary large object) qui contient certaines informations pour le gestionnaire de protocole MAPI. Le fournisseur de magasin associe cet OBJET BLOB à chaque URL MAPI et l’envoie lors de l’envoi de l’URL MAPI à l’indexeur. Le format de l’OBJET BLOB est le suivant : 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Le fournisseur du magasin doit écrire ces valeurs dans l’objet BLOB dans l’ordre indiqué. Le tableau suivant décrit chaque champ de l’OBJET BLOB.

|Élément | Description|
|:----|:-----------|  
|*dwVersion* |Il s’agit de la version des données envoyées. Actuellement, cette valeur est 1.|
|*dwFlags* |Réservé à une utilisation future. Actuellement, cette valeur doit être 0.|
|*cbProfileName* |Taille du nom du profil, en octets. Ces informations sont utiles pour que le gestionnaire de protocole MAPI sache quel profil utiliser lors de l’indexation de l’élément.|
|*wszProfileName* |Chaîne Unicode terminée par une valeur Null qui contient le nom du profil.|
|*cbProviderItemID* |Taille de l’ID d’élément du fournisseur, en octets. Le fournisseur du magasin doit envoyer uniquement l’ID d’élément du fournisseur pour les dossiers, afin d’empêcher l’ouverture de dossiers supplémentaires pour obtenir ces informations.|
|*wszProviderItemID* |Chaîne Unicode terminée par une valeur Null avec l’ID d’élément de fournisseur qui identifie de façon unique l’élément dans le magasin.|
    
## <a name="see-also"></a>Voir aussi

- [À propos de Notification-Based l’indexation du Store](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

