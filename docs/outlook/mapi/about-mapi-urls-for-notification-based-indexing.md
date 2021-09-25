---
title: À propos des URL MAPI pour lNotification-Based indexation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: f51ddada87a68a13322641b21acda317a8ce5442
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588286"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>À propos des URL MAPI pour lNotification-Based indexation

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un fournisseur de magasin avertit un indexeur qu’un objet est prêt pour l’indexation, il génère une URL MAPI qui identifie de manière unique l’objet dans le handler de protocole MAPI. Les URL MAPI sont codées en Unicode et ont le format suivant : 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

Le tableau suivant décrit les différentes parties d’une URL classique.

|Élément | Description|
|:----|:-----------|  
|*SID* |Identificateur de sécurité de l’utilisateur actuel.| 
|*StoreDisplayName* |Chaîne qui spécifie le nom complet de l’utilisateur sur ce magasin.|
|*HashNumber* |Valeur **DWORD dans** une représentation hexadécimale calculée en fonction de l’ID d’entrée de la boutique ou de la signature de mappage de la boutique. Cette valeur est stockée dans le Registre et sera utilisée ultérieurement pour identifier le magasin dans le handler de protocole MAPI.<br/><br/>Ce nombre doit être calculé de manière à minimiser les collisions avec d’autres magasins. Pour l’algorithme que Microsoft Outlook utilise pour calculer le numéro de hachage, voir [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Nombre qui identifie le type de la boutique qui contient l’objet à indexer. Les valeurs possibles sont les suivantes :<br/>- 0 - Magasin par défaut.<br/><br/>- 1 - Magasin de délégués, utilisé pour les éléments délégués mis en cache localement.<br/><br/>- 2 - Dossiers publics, utilisés pour les favoris des dossiers publics.<br/><br/>**REMARQUE**: si la boutique est en cours d’analyse au lieu d’être poussée, la valeur utilisée est le caractère *X*.| 
|*FolderNameA/.../FolderNameN* |Chemin d’accès de la racine du IPM_SUBTREE au dossier ou au message. Par exemple, un message dans  le dossier **Famille** sous Boîte de réception a Boîte **de réception/Famille** pour ce paramètre. |
|*EntryIDEncoded* |ID d’entrée MAPI pour l’élément codé en tant que chaîne Unicode. Consultez la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont codés. Pour plus d’informations sur l’algorithme permettant de coder l’ID d’entrée, voir [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**REMARQUE**: lorsqu’il est considéré comme du texte, cet ID d’entrée codée apparaît sous forme de caractères ou de zones hangul aléatoires conformes à l’algorithme, en fonction des polices disponibles.  |
|*AttachIDEncoded* |ID de pièce jointe codé en tant que chaîne Unicode. Consultez la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont codés. Pour plus d’informations sur l’algorithme permettant de coder l’ID d’entrée, voir [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**REMARQUE**: lorsqu’il est considéré comme du texte, cet ID d’entrée codée apparaît sous forme de caractères ou de zones hangul aléatoires conformes à l’algorithme, en fonction des polices disponibles. |
|*FileName* |Nom du fichier joint tel qu’il apparaît dans le message.|
    
## <a name="examples-of-mapi-urls"></a>Exemples d’URL MAPI

Voici quelques exemples d’URL MAPI.
  
- URL MAPI pour un dossier : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL MAPI pour un message : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL MAPI pour une pièce jointe : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caractères spéciaux

Certains caractères sont codés s’ils apparaissent dans le message ou la pièce jointe. L’exemple suivant montre les caractères codés dans une URL MAPI :
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob associé à chaque URL MAPI

Lors de la poussée d’une URL MAPI pour un objet à indexer, un fournisseur de magasins crée également un objet BLOB (Binary Large Object) qui contient certaines informations pour le handleur de protocole MAPI. Le fournisseur de magasin associe ce BLOB à chaque URL MAPI et l’envoie lors de l’envoi de l’URL MAPI à l’indexeur. Le format du BLOB est le suivant : 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Le fournisseur de magasin doit écrire ces valeurs dans le BLOB dans l’ordre indiqué. Le tableau suivant décrit chaque champ de l’objet BLOB.

|Élément | Description|
|:----|:-----------|  
|*dwVersion* |Il s’agit de la version des données envoyées. Actuellement, cette valeur est 1.|
|*dwFlags* |Réservé à une utilisation future. Actuellement, cette valeur doit être 0.|
|*cbProfileName* |Taille du nom du profil, en octets. Ces informations sont utiles pour que le responsable du protocole MAPI sache quel profil utiliser lors de l’indexation de l’élément.|
|*wszProfileName* |Chaîne Unicode terminée par null qui contient le nom du profil.|
|*cbProviderItemID* |Taille de l’ID de l’élément fournisseur, en octets. Le fournisseur de magasins doit envoyer uniquement l’ID d’élément de fournisseur pour les dossiers, afin d’empêcher l’ouverture de dossiers supplémentaires pour obtenir ces informations.|
|*wszProviderItemID* |Chaîne Unicode terminée par null avec l’ID d’élément fournisseur qui identifie de manière unique l’élément dans la banque.|
    
## <a name="see-also"></a>Voir aussi

- [À propos Notification-Based'indexation du Store](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

