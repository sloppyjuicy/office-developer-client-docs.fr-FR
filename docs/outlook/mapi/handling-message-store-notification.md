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
  
Pour vous inscrire aux notifications de banque de messages, appelez la méthode [IMAPISession:: Advise](imapisession-advise.md) ou [IMsgStore:: Advise](imsgstore-advise.md) et spécifiez une banque de messages, un dossier ou un identificateur d'entrée de message dans le contenu du paramètre _lpEntryID_ . Les fournisseurs de banques de messages prennent en charge les notifications d'objet et de table. Que vous vous inscriviez avec des objets de banque de messages particuliers, avec les tables de hiérarchie de dossiers et de contenu qui décrivent ces objets, ou avec les objets et les tables, dépend des notifications que vous vous attendez à voir, des appels que vous effectuez pour effectuer des opérations et de la procédure le fournisseur de banque de messages prend en charge la notification. 
  
Étant donné que MAPI autorise la flexibilité de la prise en charge des notifications par les fournisseurs, sachez que vous ne recevrez pas toujours le même type de notification en réponse à un événement particulier de tous les fournisseurs de banques de messages. Certains fournisseurs de banques de messages ne prennent pas en charge les notifications. Pour déterminer si la Banque de messages que vous utilisez prend en charge la notification, recherchez le bit STORE_NOTIFY_OK dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
À une extrémité du spectre des fournisseurs de banques de messages qui prennent en charge la notification sont les fournisseurs qui génèrent des notifications «enrichies»; ces fournisseurs envoient des notifications descriptives pour toutes les sources de notification enregistrées. Aux autres terminaisons sont les fournisseurs de banques de messages qui prennent en charge les notifications limitées; ces fournisseurs envoient des notifications générales pour un nombre restreint de sources de notification. 
  
Par exemple, si vous copiez un message dans un dossier avec lequel vous avez été inscrit pour recevoir des notifications de déplacement d'objets et d'objet, il se peut que vous receviez ou non la notification copiée d'objet. Le fait que vous le receviez ou non dépend des éléments suivants:
  
- La méthode que vous avez appelée pour effectuer la copie. Il peut s'agir de [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIProp:: CopyTo](imapiprop-copyto.md)ou [IMAPIProp:: CopyProps](imapiprop-copyprops.md).
    
- Implémentation par le fournisseur de banque de messages de la méthode de copie.
    
- Si le fournisseur de banque de messages prend ou non en charge les notifications copiées par l'objet sur les dossiers.
    
Étant donné qu'il n'existe pas de recommandations strictes qui décrivent la manière d'implémenter la notification d'événement pour les fournisseurs de banques de messages, les clients ne peuvent pas être cohérents. MAPI effectue des recommandations sur la façon dont les fournisseurs de banque de messages implémentent la notification d'événement et le tableau suivant présente ces recommandations. Lisez le tableau comme suit: une fois que vous avez effectué l'opération dans la première colonne, attendez la réception d'une notification du type indiqué dans la deuxième colonne si vous avez inscrit pour ce type avec l'objet répertorié dans la troisième colonne. Par exemple, une fois que vous avez créé un dossier, vous ne recevrez une notification _fnevObjectCreated_ que si vous vous êtes inscrit pour les notifications de _fnevObjectCreated_ avec la Banque de messages. 
  
|**Opération**|**Type d’événement**|**Source de notification**|
|:-----|:-----|:-----|
|Créer un dossier  <br/> | _fnevObjectCreated_ <br/> |Banque de messages  <br/> |
|Supprimer un dossier  <br/> | _fnevObjectDeleted_ <br/> |Dossier supprimé de la Banque de messages  <br/> |
|Déplacer un dossier d'un dossier à un autre  <br/> | _fnevObjectMoved_ <br/> |Dossier déplacé dans la Banque de messages  <br/> |
|Copier un dossier d'un dossier à un autre  <br/> | _fnevObjectCopied_ <br/> |Banque de messages et dossier copié (aucune notification _fnevObjectCreated_ envoyée pour la nouvelle copie du dossier)  <br/> |
|Modification d'une propriété de dossier calculée (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Dossier de la Banque de messages modifiée (aucune notification au dossier parent)  <br/> |
|Créer un message  <br/> | _fnevObjectCreated_ <br/> |Banque de messages  <br/> |
|Supprimer un message, entraînant une modification dans la propriété **PR_CONTENT_COUNT** du dossier parent  <br/> | _fnevObjectDeleted_ <br/> |Message de magasin de messages supprimé  <br/> |
|Déplacer un message d'un dossier à un autre  <br/> | _fnevObjectMoved_ <br/> |Message déplacé de banque de messages  <br/> |
|Copier un message d'un dossier à un autre  <br/> | _fnevObjectCopied_ <br/> |Message copié de la Banque de messages (aucune notification _fnevObjectCreated_ pour la nouvelle copie du message)  <br/> |
|Enregistrer un message, entraînant une modification dans la propriété **PR_CONTENT_COUNT** du dossier parent  <br/> | _fnevObjectCreated_ <br/> |Banque de messages lors du premier enregistrement uniquement  <br/> |
|Enregistrer un message  <br/> | _fnevObjectModified_ <br/> |Banque de messages lors des enregistrements après le premier message enregistrement modifié (aucune notification au dossier parent)  <br/> |
|Effectuer une opération de recherche  <br/> | _fnevSearchComplete_ <br/> |Dossier de recherche de banque de messages  <br/> |
|Nouveau message  <br/> | _fnevNewMail_ <br/> |Banque de messages  <br/> |
   
> [!NOTE]
> Lorsque vous recevez une notification de modification d'objet, n'oubliez pas que la partie de tableau de la balise de propriété de la structure [OBJECT_NOTIFICATION](object_notification.md) vers laquelle pointe le paramètre _lpNotifications_ dans l'appel **OnNotify** peut être null ou non. Les fournisseurs de banque de messages ne sont pas requis pour insérer des informations de propriété dans ce tableau, et la plupart ne le font pas. Assurez-vous que votre méthode **OnNotify** peut gérer le cas où le pointeur _lpPropTagArray_ est null. 
  
Pour la plupart, si ce n'est pas toutes les notifications d'objet, mettez à jour l'affichage du dossier ou des dossiers affectés.
  

