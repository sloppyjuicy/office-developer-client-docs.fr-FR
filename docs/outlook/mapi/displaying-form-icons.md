---
title: Affichage des icônes de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7ac8026489b06031e07ab4b2978c9ece04063bb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579143"
---
# <a name="displaying-form-icons"></a>Affichage des icônes de formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous affichez une liste des messages dans un dossier, il est utile pour les utilisateurs si vous distinguer les messages avec les classes de message personnalisées à partir de l’IPM standard. Notez les messages. Classes de message personnalisées correspondent aux serveurs de formulaire et les serveurs de formulaire permettent d’icônes pour représenter elle-même. Vous pouvez afficher ces icônes dans la liste des messages pour avertir les utilisateurs de la classe de message de chaque message avant que l’utilisateur ouvre les messages. En règle générale, l’icône de la propriété du formulaire **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) est celui qui doit être affiché dans la liste des messages. Formulaires ont également une propriété **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) qui peut être affichée lorsque le formulaire est réduit dans une feuille de propriétés.
  
 **Pour obtenir une icône pour une classe de message sans activer le serveur de formulaire pour cette classe de message**
  
1. Appelez la méthode [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) pour obtenir un pointeur vers une [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface. 
    
2. Appelez la méthode [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) pour obtenir un pointeur vers une [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface. 
    
3. Appelez la méthode [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) pour obtenir un handle d’icône. 
    
L’icône peut ensuite être affichée à l’aide des API Win32 standard.
  
> [!IMPORTANT]
> Une fois que l’icône d’une classe de message, vérifiez tous leurs efforts pour mettre en cache cette icône. Ne pas de mise en cache des icônes sérieusement affecte les performances des applications clientes. Lors de la mise en cache des icônes, veillez aux relations entre les classes de messages et leurs sous-classes. Par exemple, si le formulaire IPM. Classe de message Note.Meeting.Cancel se répercuter dans IPM. Remarque, ne supposent que toutes les sous-classes de IPM. Remarque doit utiliser l’icône pour IPM. Note. 
  

