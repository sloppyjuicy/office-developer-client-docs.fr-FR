---
title: À propos des URL MAPI pour l'indexation basée sur les notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422480"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>À propos des URL MAPI pour l'indexation basée sur les notifications

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un fournisseur de banque avertit un indexeur qu'un objet est prêt pour l'indexation, il génère une URL MAPI qui identifie de manière unique l'objet dans le gestionnaire de protocole MAPI. Les URL MAPI sont codées au format Unicode et ont le format suivant: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

Le tableau suivant décrit les différentes parties d'une URL standard.

|Quitter | Description|
|:----|:-----------|  
|*SID* |Identificateur de sécurité de l'utilisateur actuel.| 
|*StoreDisplayName* |Valeur de type String qui spécifie le nom d'affichage de l'utilisateur sur ce magasin.|
|*HashNumber* |**DWORD** en représentation hexadécimale calculée en fonction de l'ID d'entrée de banque ou de la signature de mappage de banque. Cette valeur est stockée dans le registre et sera utilisée ultérieurement pour identifier le magasin dans le gestionnaire de protocole MAPI.<br/><br/>Ce nombre doit être calculé d'une manière qui minimise les conflits avec d'autres magasins. Pour l'algorithme que Microsoft Outlook utilise pour calculer le numéro de hachage, voir [algorithme pour calculer le numéro de hachage de magasin](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Numéro qui identifie le type de la Banque contenant l'objet à indexer. Les valeurs possibles sont les suivantes :<br/>-0-Banque par défaut.<br/><br/>-1-Banque de délégués, utilisée pour les éléments délégués mis en cache localement.<br/><br/>-2-dossiers publics, utilisés pour les favoris des dossiers publics.<br/><br/>**Remarque**: si la Banque est en cours d'analyse au lieu d'être envoyée, la valeur utilisée est le caractère*X*.| 
|*FolderNameA/.../FolderNameN* |Chemin d'accès à la racine de l'arborescence IPM_SUBTREE vers le dossier ou le message. Par exemple, un message dans le dossier **famille** sous **boîte de réception** dispose de la boîte de **réception/famille** de ce paramètre. |
|*EntryIDEncoded* |ID d'entrée MAPI pour l'élément encodé en tant que chaîne Unicode. Consultez la section suivante «caractères spéciaux» pour plus d'informations sur la façon dont certains caractères spéciaux sont codés. Pour plus d'informations sur l'algorithme permettant de coder l'ID d'entrée, voir [algorithme pour coder les ID d'entrée et les ID de pièces jointes](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Remarque**: lorsqu'il est affiché en tant que texte, cet ID d'entrée codé apparaît sous la forme de caractères Hangul aléatoires ou de zones conformes à l'algorithme, en fonction des polices disponibles.  |
|*AttachIDEncoded* |ID de la pièce jointe codée en tant que chaîne Unicode. Consultez la section suivante «caractères spéciaux» pour plus d'informations sur la façon dont certains caractères spéciaux sont codés. Pour plus d'informations sur l'algorithme permettant de coder l'ID d'entrée, voir [algorithme pour coder les ID d'entrée et les ID de pièces jointes](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Remarque**: lorsqu'il est affiché en tant que texte, cet ID d'entrée codé apparaît sous la forme de caractères Hangul aléatoires ou de zones conformes à l'algorithme, en fonction des polices disponibles. |
|*FileName* |Nom du fichier de pièce jointe, tel qu'il apparaît dans le message.|
    
## <a name="examples-of-mapi-urls"></a>Exemples d'URL MAPI

Voici quelques exemples d'URL MAPI.
  
- URL MAPI pour un dossier: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL MAPI pour un message: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL MAPI pour une pièce jointe: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caractères spéciaux

Certains caractères sont encodés s'ils apparaissent dans le message ou dans une pièce jointe. Les caractères suivants sont codés dans une URL MAPI:
  
- % >% 25
    
- />% 2F 
    
- \ >% 5C 
    
- \*>% 2A 
    
- ? >% 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Objet BLOB associé à chaque URL MAPI

Lors du push d'une URL MAPI pour qu'un objet soit indexé, un fournisseur de banque d'informations crée également un objet BLOB (Binary Large Object) contenant certaines informations pour le gestionnaire de protocole MAPI. Le fournisseur de banque d'adresses associe cet objet BLOB à chaque URL MAPI et l'envoie lors du transfert de l'URL MAPI vers l'indexeur. Le format de l'objet BLOB est le suivant: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Le fournisseur de banque d'données doit écrire ces valeurs dans l'objet BLOB dans l'ordre indiqué. Le tableau suivant décrit chaque champ du BLOB.

|Quitter | Description|
|:----|:-----------|  
|*dwVersion* |Il s'agit de la version des données envoyées. Actuellement, cette valeur est 1.|
|*dwFlags* |Réservé à une utilisation future. Actuellement, cette valeur doit être égale à 0.|
|*cbProfileName* |Taille du nom de profil, en octets. Ces informations sont utiles pour que le gestionnaire de protocole MAPI sache quel profil utiliser lors de l'indexation de l'élément.|
|*wszProfileName* |Chaîne Unicode terminée par un caractère null qui contient le nom du profil.|
|*cbProviderItemID* |Taille de l'ID d'élément de fournisseur, en octets. Le fournisseur de banque d'informations doit envoyer uniquement l'ID d'élément de fournisseur pour les dossiers, afin d'empêcher l'ouverture de dossiers supplémentaires pour obtenir ces informations.|
|*wszProviderItemID* |Chaîne Unicode terminée par un caractère NULL avec l'ID d'élément de fournisseur qui identifie de façon unique l'élément dans le magasin.|
    
## <a name="see-also"></a>Voir aussi

- [À propos de l'indexation du magasin basé sur les notifications](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

