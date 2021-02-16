---
title: Gestion des notifications de la banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428024"
---
# <a name="handling-message-store-notification"></a>Gestion des notifications de la banque de messages
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour vous inscrire aux notifications de la boutique de messages, appelez la méthode [IMAPISession::Advise](imapisession-advise.md) ou [IMsgStore::Advise](imsgstore-advise.md) et spécifiez un identificateur d’entrée de message, de dossier ou de magasin de messages dans le contenu du paramètre _lpEntryID._ Les fournisseurs de magasins de messages supportent à la fois les notifications d’objet et de table. Que vous vous enregistriez avec des objets de magasin de messages particuliers, avec la hiérarchie de dossiers et les tables de contenu qui décrivent ces objets, ou avec les objets et les tables dépend des notifications que vous prévoyez de voir, des appels que vous effectuez pour effectuer des opérations et de la façon dont le fournisseur de magasin de messages prend en charge la notification. 
  
Étant donné que MAPI offre de la flexibilité dans la prise en charge des notifications par les fournisseurs, sachez que vous ne recevrez pas toujours le même type de notification en réponse à un événement particulier de la part de tous les fournisseurs de magasins de messages. Certains fournisseurs de magasins de messages ne supportent pas du tout les notifications. Pour déterminer si la boutique de messages que vous utilisez prend en charge la notification, recherchez le bit STORE_NOTIFY_OK dans sa **propriété PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)
  
À une extrémité de la gamme des fournisseurs de magasins de messages qui supportent la notification sont les fournisseurs qui génèrent des notifications « enrichies » ; ces fournisseurs envoient des notifications descriptives pour toutes les sources de conseil enregistrées. À l’autre extrémité se retrouvent les fournisseurs de magasins de messages qui ne peuvent pas recevoir de notifications limitées. ces fournisseurs envoient des notifications générales pour un nombre restreint de sources de conseil. 
  
Par exemple, si vous copiez un message dans un dossier avec lequel vous vous êtes inscrit pour recevoir des notifications d’objet copié et de déplacé d’objet, vous pouvez recevoir ou non la notification copiée d’objet. La réception ou non dépend des cas ci-après :
  
- Méthode que vous avez appelée pour effectuer la copie. Cela peut être [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)ou [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Comment le fournisseur de magasin de messages implémente la méthode de copie.
    
- Si le fournisseur de magasin de messages prend en charge les notifications copiées d’objet sur les dossiers.
    
Étant donné qu’il n’existe aucune directive stricte décrivent comment implémenter la notification d’événement pour les fournisseurs de magasins de messages, les clients ne peuvent pas s’attendre à un comportement cohérent. MAPI fait des recommandations sur la façon dont les fournisseurs de magasins de messages implémentent la notification d’événement et le tableau suivant décrit ces recommandations. Lisez le tableau comme suit : après avoir effectué l’opération dans la première colonne, attendez-vous à recevoir une notification du type répertorié dans la deuxième colonne si vous vous êtes inscrit pour ce type avec l’objet répertorié dans la troisième colonne. Par exemple, une fois que vous avez créé un dossier, vous recevrez une notification  _fnevObjectCreated_ uniquement si vous avez inscrit des notifications  _fnevObjectCreated_ auprès de la boutique de messages. 
  
|**Opération**|**Type d’événement**|**Source de conseil**|
|:-----|:-----|:-----|
|Créer un dossier  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages  <br/> |
|Supprimer un dossier  <br/> | _fnevObjectDeleted_ <br/> |Dossier supprimé de la boutique de messages  <br/> |
|Déplacer un dossier d’un dossier vers un autre  <br/> | _fnevObjectMoved_ <br/> |Dossier déplacé de la boutique de messages  <br/> |
|Copier un dossier d’un dossier vers un autre  <br/> | _fnevObjectCopied_ <br/> |Magasin de messages et dossier copié (aucune notification  _fnevObjectCreated_ envoyée pour la nouvelle copie du dossier)  <br/> |
|Modification dans une propriété de dossier calculée (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Dossier modifié de la boutique de messages (aucune notification au dossier parent)  <br/> |
|Créer un message  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages  <br/> |
|Supprimer un message, entraînant une modification de la propriété de PR_CONTENT_COUNT **parent**  <br/> | _fnevObjectDeleted_ <br/> |Message supprimé de la boutique de messages  <br/> |
|Déplacer un message d’un dossier vers un autre  <br/> | _fnevObjectMoved_ <br/> |Message déplacé de la boutique de messages  <br/> |
|Copier un message d’un dossier vers un autre  <br/> | _fnevObjectCopied_ <br/> |Message de la boutique de messages - Message copié (aucune notification  _fnevObjectCreated_ pour la nouvelle copie du message)  <br/> |
|Enregistrer un message, entraînant une modification de la propriété PR_CONTENT_COUNT dossier **parent**  <br/> | _fnevObjectCreated_ <br/> |Magasin de messages lors du premier sauvegarde uniquement  <br/> |
|Enregistrer un message  <br/> | _fnevObjectModified_ <br/> |Message store on saves after the first save Changed message (No notification to parent folder)  <br/> |
|Effectuer une opération de recherche  <br/> | _fnevSearchComplete_ <br/> |Dossier de recherche de la boutique de messages  <br/> |
|Nouveau message  <br/> | _fnevNewMail_ <br/> |Magasin de messages  <br/> |
   
> [!NOTE]
> Lorsque vous recevez une notification de modification d’objet, n’oubliez pas que la partie tableau de balises de propriétés de la structure [OBJECT_NOTIFICATION](object_notification.md) pointée par le paramètre  _lpNotifications_ dans l’appel **OnNotify** peut ou non être NULL. Les fournisseurs de magasins de messages ne sont pas obligés d’insérer des informations de propriété dans ce tableau et la plupart d’entre eux ne le font pas. Assurez-vous **que votre méthode OnNotify** peut gérer le cas où le pointeur  _lpPropTagArray_ est NULL. 
  
Pour la plupart, si ce n’est toutes les notifications d’objet, mettez à jour l’affichage du ou des dossiers affectés.
  

