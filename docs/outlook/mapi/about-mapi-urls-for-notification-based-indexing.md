---
title: À propos des URL MAPI pour l’indexation basée sur une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 57868996f95cfb135298378d2638bc57b2e69977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583672"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>À propos des URL MAPI pour l’indexation basée sur une notification

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un fournisseur de magasins signale un indexeur qu’un objet est prêt pour l’indexation, elle génère une URL MAPI qui identifie l’objet dans le Gestionnaire de protocole MAPI. MAPI URL sont codées au format Unicode et présentent le format suivant : 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

Le tableau suivant décrit les différentes parties d’une URL par défaut.

|Élément | Description|
|:----|:-----------|  
|*SID* |Identificateur de sécurité de l’utilisateur actuel.| 
|*StoreDisplayName* |Chaîne qui spécifie le nom complet de l’utilisateur de cette banque.|
|*Numéro_hachage* |Une **valeur DWORD** de représentation hexadécimale qui est calculée basé sur l’identificateur d’entrée de magasin ou la signature de mappage de magasin. Cette valeur est stockée dans le Registre et servira ensuite à identifier la banque dans le Gestionnaire de protocole MAPI.<br/><br/>Ce numéro doit être calculé d’une manière qui minimise les collisions avec d’autres magasins. Pour l’algorithme que Microsoft Outlook utilise pour calculer le nombre de hachage, voir [algorithme pour calculer le nombre de hachage magasin](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Numéro qui identifie le type de la banque qui contient l’objet à indexer. Les valeurs possibles sont les suivantes :<br/>-0 - banque par défaut.<br/><br/>-1 - banque déléguée, utilisée pour les éléments de délégué mis en cache localement.<br/><br/>-2 - les dossiers publics, utilisés pour le dossier public Favoris.<br/><br/>**Remarque**: si le magasin est en cours d’analyse au lieu de poussée (push), la valeur qui est utilisée est le caractère*X*.| 
|*FolderNameA/.../FolderNameN* |Le chemin d’accès à la racine de l’arborescence IPM_SUBTREE du dossier ou du message. Par exemple, un message dans le dossier **famille** sous **boîte de réception** **a/Famille de boîte de réception** pour ce paramètre. |
|*EntryIDEncoded* |Identificateur d’entrée MAPI pour l’élément codé sous forme de chaîne Unicode. Voir la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont codées. Pour plus d’informations sur l’algorithme pour coder l’identificateur d’entrée, voir [algorithme pour coder les identificateurs d’entrée et des ID de pièce jointe](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Remarque**: lorsqu’ils sont affichés sous forme de texte, cela codé entrée ID apparaît sous la forme des caractères Hangul en caractères aléatoire ou des zones conformément à l’algorithme, en fonction des polices disponibles.  |
|*AttachIDEncoded* |ID de pièce jointe codé sous forme de chaîne Unicode. Voir la section suivante « Caractères spéciaux » pour plus d’informations sur la façon dont certains caractères spéciaux sont codées. Pour plus d’informations sur l’algorithme pour coder l’identificateur d’entrée, voir [algorithme pour coder les identificateurs d’entrée et des ID de pièce jointe](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Remarque**: lorsqu’ils sont affichés sous forme de texte, cela codé entrée ID apparaît sous la forme des caractères Hangul en caractères aléatoire ou des zones conformément à l’algorithme, en fonction des polices disponibles. |
|*FileName* |Nom de la pièce jointe du fichier, tel qu’il apparaît dans le message.|
    
## <a name="examples-of-mapi-urls"></a>Exemples d’URL MAPI

Voici quelques exemples d’URL MAPI.
  
- MAPI l’URL d’un dossier : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL de MAPI pour un message : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL de MAPI pour une pièce jointe : 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caractères spéciaux

Certains caractères sont codés s’ils apparaissent dans le message ou d’une pièce jointe. L’exemple suivant montre les caractères sont codés dans une URL MAPI :
  
- % > % 25
    
- / > % 2F 
    
- \ > 5 % C 
    
- \*> % 2 
    
- ? > % 3 
    
## <a name="blob-associated-with-each-mapi-url"></a>BLOB associée à chaque URL MAPI

Lors de l’envoi d’une URL de MAPI pour un objet à indexer, un fournisseur de magasins crée également un grand BLOB (binary object) qui contient des informations pour le Gestionnaire de protocole MAPI. Le fournisseur de banque associe ce BLOB à chaque URL MAPI et les envoie lors de la distribution de l’URL de MAPI à l’indexeur. Le format de l’objet BLOB est comme suit : 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Le fournisseur de banque doit écrire ces valeurs dans l’objet BLOB dans l’ordre indiqué. Le tableau suivant décrit chaque champ de l’objet BLOB.

|Élément | Description|
|:----|:-----------|  
|*dwVersion* |Il s’agit de la version des données envoyées. Actuellement, cette valeur est 1.|
|*dwFlags* |Réservé à une utilisation ultérieure. Actuellement, cette valeur doit être 0.|
|*cbProfileName* |La taille du nom du profil, en octets. Ces informations sont utiles pour le Gestionnaire de protocole MAPI à connaître le profil à utiliser lors de l’indexation de l’élément.|
|*wszProfileName* |Unicode chaîne qui contient le nom du profil.|
|*cbProviderItemID* |Taille de l’ID d’élément fournisseur, en octets. Le fournisseur de banque doit envoyer uniquement le fournisseur d’ID d’élément pour les dossiers, afin d’empêcher l’ouverture des dossiers supplémentaires pour obtenir ces informations.|
|*wszProviderItemID* |Chaîne Unicode terminée avec l’ID d’élément fournisseur qui identifie l’élément dans le magasin|
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’indexation de magasin basée sur une notification](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

