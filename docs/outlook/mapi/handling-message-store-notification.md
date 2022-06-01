---
title: Gestion des notifications de la banque de messages
description: Cet article décrit l’inscription et la gestion des notifications du magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
ms.openlocfilehash: 4889d71320986a471878420a1fb0aeaaa86e528a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817304"
---
# <a name="handling-message-store-notification"></a>Gestion des notifications de la banque de messages
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour vous inscrire aux notifications du magasin de messages, appelez la méthode [IMAPISession::Advise](imapisession-advise.md) ou [IMsgStore::Advise](imsgstore-advise.md) et spécifiez un magasin de messages, un dossier ou un identificateur d’entrée de message dans le contenu du paramètre  _lpEntryID_ . Les fournisseurs de magasin de messages prennent en charge les notifications d’objet et de table. Que vous vous inscrivez auprès d’objets de magasin de messages particuliers, avec la hiérarchie de dossiers et les tables de contenu qui décrivent ces objets, ou avec les objets et les tables, cela dépend des notifications que vous prévoyez de voir, des appels que vous effectuez pour effectuer des opérations et de la façon dont le fournisseur du magasin de messages prend en charge la notification. 
  
Étant donné que MAPI offre une flexibilité quant à la façon dont les fournisseurs prennent en charge les notifications, sachez que vous ne recevrez pas toujours le même type de notification en réponse à un événement particulier de la part de tous les fournisseurs de magasins de messages. Certains fournisseurs de magasins de messages ne prennent pas en charge les notifications. Pour déterminer si le magasin de messages que vous utilisez prend en charge la notification, recherchez le bit STORE_NOTIFY_OK dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
À une extrémité du spectre des fournisseurs de magasins de messages qui prennent en charge les notifications sont les fournisseurs qui génèrent des notifications « riches » ; ces fournisseurs envoient des notifications descriptives pour toutes les sources de conseils inscrites. À l’autre extrémité se trouvent les fournisseurs de magasins de messages qui prennent en charge les notifications limitées ; ces fournisseurs envoient des notifications générales pour un nombre restreint de sources de conseils. 
  
Par exemple, si vous copiez un message dans un dossier avec lequel vous vous êtes inscrit pour recevoir à la fois des notifications copiées et déplacées d’objet, vous pouvez ou non recevoir la notification copiée par l’objet. Le fait que vous le receviez ou non dépend des éléments :
  
- Méthode que vous avez appelée pour effectuer la copie. Il peut s’agir de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md) ou [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Comment le fournisseur du magasin de messages implémente la méthode de copie.
    
- Indique si le fournisseur du magasin de messages prend en charge les notifications copiées par objet sur les dossiers.
    
Étant donné qu’il n’existe aucune directive stricte décrivant comment implémenter la notification d’événement pour les fournisseurs de magasins de messages, les clients ne peuvent pas s’attendre à un comportement cohérent. MAPI fait des recommandations sur la façon dont les fournisseurs de magasins de messages implémentent la notification d’événements et le tableau suivant décrit ces recommandations. Lisez le tableau comme suit : après avoir effectué l’opération dans la première colonne, attendez-vous à recevoir une notification du type répertorié dans la deuxième colonne si vous vous êtes inscrit pour ce type avec l’objet répertorié dans la troisième colonne. Par exemple, une fois que vous avez créé un dossier, vous recevez une notification  _fnevObjectCreated_ uniquement si vous vous êtes inscrit aux notifications  _fnevObjectCreated_ auprès du magasin de messages. 
  
|**Opération**|**Type d’événement**|**Conseiller la source**|
|:-----|:-----|:-----|
|Créer un dossier  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages  <br/> |
|Supprimer un dossier  <br/> | _fnevObjectDeleted_ <br/> |Dossier supprimé du magasin de messages  <br/> |
|Déplacer un dossier d’un dossier vers un autre  <br/> | _fnevObjectMoved_ <br/> |Dossier déplacé du magasin de messages  <br/> |
|Copier un dossier d’un dossier vers un autre  <br/> | _fnevObjectCopied_ <br/> |Magasin de messages et dossier copié (aucune notification  _fnevObjectCreated_ envoyée pour la nouvelle copie du dossier)  <br/> |
|Modification dans une propriété de dossier calculée (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Dossier Modifié du magasin de messages (aucune notification au dossier parent)  <br/> |
|Créer un message  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages  <br/> |
|Supprimer un message, ce qui entraîne une modification de la propriété **PR_CONTENT_COUNT** du dossier parent  <br/> | _fnevObjectDeleted_ <br/> |Message supprimé du magasin de messages  <br/> |
|Déplacer un message d’un dossier vers un autre  <br/> | _fnevObjectMoved_ <br/> |Message déplacé dans le magasin de messages  <br/> |
|Copier un message d’un dossier vers un autre  <br/> | _fnevObjectCopied_ <br/> |Message copié du magasin de messages (aucune notification  _fnevObjectCreated_ pour la nouvelle copie du message)  <br/> |
|Enregistrer un message, ce qui entraîne une modification de la propriété **PR_CONTENT_COUNT** du dossier parent  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages lors de la première enregistrement uniquement  <br/> |
|Enregistrer un message  <br/> | _fnevObjectModified_ <br/> |Magasin de messages sur les sauvegardes après le premier message d’enregistrement Modifié (aucune notification au dossier parent)  <br/> |
|Effectuer une opération de recherche  <br/> | _fnevSearchComplete_ <br/> |Dossier de recherche du magasin de messages  <br/> |
|Nouveau message  <br/> | _fnevNewMail_ <br/> |Magasin de messages  <br/> |
   
> [!NOTE]
> Lorsque vous recevez une notification de modification d’objet, n’oubliez pas que la partie du tableau de balises de propriétés de la structure [OBJECT_NOTIFICATION](object_notification.md) pointée par le paramètre  _lpNotifications_ dans l’appel **OnNotify** peut être null ou non. Les fournisseurs de magasin de messages ne sont pas tenus d’insérer des informations de propriété dans ce tableau et la plupart ne le font pas. Assurez-vous que votre méthode **OnNotify** peut gérer le cas où le pointeur  _lpPropTagArray_ a la valeur NULL. 
  
Pour la plupart, si ce n’est pas toutes les notifications d’objet, mettez à jour l’affichage du dossier ou des dossiers concernés.
  

