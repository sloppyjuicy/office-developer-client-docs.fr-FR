---
title: Gestion de notification de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783433"
---
# <a name="handling-message-store-notification"></a>Gestion de notification de banque de messages
  
**S’applique à**: Outlook 
  
Pour vous inscrire pour les notifications de banque de messages, appelez le [IMAPISession::Advise](imapisession-advise.md) ou le [IMsgStore::Advise](imsgstore-advise.md) et spécifiez une banque de messages, un dossier ou un identificateur d’entrée du message dans le contenu du paramètre _lpEntryID_ . Fournisseurs de banque de messages prennent en charge les notifications d’objet et de tableau. Si vous enregistrez avec les objets de banque de message particulier, les tables de hiérarchie et le contenu de dossier qui décrivent ces objets ou les deux objets et tables varie selon les notifications, vous devriez voir, les appels pour effectuer des opérations, et comment le fournisseur de banque de message prend en charge la notification. 
  
Étant donné que MAPI permet une grande flexibilité comment fournisseurs prennent en charge les notifications, sachez que vous ne recevrez pas toujours de même type de notification en réponse à un événement spécifique à partir de tous les fournisseurs de banque de messages. Certains fournisseurs de banque de messages n’acceptent pas les notifications. Pour déterminer si la banque de messages que vous utilisez prend en charge la notification, recherchez le bit STORE_NOTIFY_OK dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
Une des extrémités du spectre de banque de messages fournisseurs qui prennent en charge les notifications sont les fournisseurs qui génèrent des notifications « riches » ; Ces fournisseurs envoient des notifications descriptives pour tous les inscrit conseiller sources. À l’autre extrémité est le message de fournisseurs de magasins qui prennent en charge les notifications limitées ; Ces fournisseurs d’envoyer des notifications générales pour un nombre limité de sources advise. 
  
Par exemple, si vous copiez un message dans un dossier avec lequel vous avez enregistré pour recevoir les deux objet copié et l’objet déplacé notifications, mais peut ne pas recevoir la notification de l’objet copié. Si vous recevez cela dépend :
  
- La méthode que vous avez appelée pour effectuer la copie. Cela peut être [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)ou [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Comment la banque de messages fournisseur implémente la méthode copy.
    
- Ou non le fournisseur de banque de message prend en charge les notifications de l’objet copié dans les dossiers.
    
Étant donné qu’aucun recommandations formelles qui décrivent comment implémenter la notification d’événement pour un message ne stockent les fournisseurs, clients ne peuvent pas s’attendent un comportement cohérent. MAPI rend des recommandations quant à la banque de messages notification d’événement fournisseurs implémenter et le tableau suivant indique les recommandations suivantes. Le tableau comme suit : après avoir effectué l’opération dans la première colonne, vous attendre à recevoir une notification du type répertorié dans la deuxième colonne si vous avez enregistré pour ce type de l’objet figurant dans la troisième colonne. Par exemple, une fois que vous avez créé un dossier, vous recevrez une notification _fnevObjectCreated_ uniquement si vous avez enregistré les notifications de _fnevObjectCreated_ avec la banque de messages. 
  
|**Opération**|**Type d’événement**|**Source de notification**|
|:-----|:-----|:-----|
|Créez un dossier  <br/> | _fnevObjectCreated_ <br/> |Banque de messages  <br/> |
|Supprimer un dossier  <br/> | _fnevObjectDeleted_ <br/> |Banque de messages dossier supprimés  <br/> |
|Déplacer un dossier d’un dossier à un autre  <br/> | _fnevObjectMoved_ <br/> |Dossier de déplacement de banque de messages  <br/> |
|Copier un dossier d’un dossier à un autre  <br/> | _fnevObjectCopied_ <br/> |Message stocker et copié le dossier (aucune notification _fnevObjectCreated_ envoyé pour la nouvelle copie du dossier)  <br/> |
|Modifier une propriété de dossier calculé (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Banque de messages dossier Changed (aucune notification au dossier parent)  <br/> |
|Créer un message  <br/> | _fnevObjectCreated_ <br/> |Banque de messages  <br/> |
|Supprimer un message, entraînant une modification dans l’objet parent **PR_CONTENT_COUNT** , propriété du folder  <br/> | _fnevObjectDeleted_ <br/> |Banque de messages supprimés message  <br/> |
|Déplacer un message d’un dossier à un autre  <br/> | _fnevObjectMoved_ <br/> |Message de déplacement de banque de messages  <br/> |
|Copier un message d’un dossier à un autre  <br/> | _fnevObjectCopied_ <br/> |Banque de messages copiés message (aucun _fnevObjectCreated_ notification de la nouvelle copie du message)  <br/> |
|Enregistrer un message, entraînant une modification dans l’objet parent **PR_CONTENT_COUNT** , propriété du folder  <br/> | _fnevObjectCreated_ <br/> |Banque de messages sur le premier enregistrement uniquement  <br/> |
|Enregistrer un message  <br/> | _fnevObjectModified_ <br/> |Banque de messages sur enregistre après le premier enregistrement Changed message (aucune notification au dossier parent)  <br/> |
|Effectuer une opération de recherche  <br/> | _fnevSearchComplete_ <br/> |Dossier de recherche de banque de messages  <br/> |
|Nouveau message  <br/> | _fnevNewMail_ <br/> |Banque de messages  <br/> |
   
> [!NOTE]
> Lorsque vous recevez une notification de l’objet modifié, n’oubliez pas que la partie de tableau de balise de propriété de la structure [OBJECT_NOTIFICATION](object_notification.md) désignée par le paramètre _lpNotifications_ dans l’appel de **OnNotify** peut ou ne peut pas être NULL. Fournisseurs de banque de messages ne sont pas nécessaire à insérer des informations sur la propriété dans ce tableau plus mais pas. Assurez-vous que votre méthode **OnNotify** peut gérer le cas où le pointeur _lpPropTagArray_ est NULL. 
  
Pour la plupart, si pas toutes les notifications d’objet, mettre à jour l’affichage de l’ou les dossiers concernés.
  

