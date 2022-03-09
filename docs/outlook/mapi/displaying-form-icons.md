---
title: Affichage des icônes de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
ms.openlocfilehash: fe322f9d8107506795e37f81d2fe833343f5fef4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378883"
---
# <a name="displaying-form-icons"></a>Affichage des icônes de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’affichage d’une liste de messages dans un dossier, il est utile pour vos utilisateurs si vous distinguez les messages avec des classes de messages personnalisées de l’IPM standard. Messages de note. Les classes de message personnalisées correspondent aux serveurs de formulaires et les serveurs de formulaire fournissent des icônes pour se représenter eux-mêmes. Vous pouvez afficher ces icônes dans la liste des messages pour alerter les utilisateurs de la classe de message de chaque message avant que l’utilisateur n’ouvre les messages. En règle générale, l’icône de la propriété **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) du formulaire est celle qui doit être affichée dans la liste des messages. Les formulaires ont **également PR_ICON** propriété ([PidTagIcon](pidtagicon-canonical-property.md)) qui peut être affichée lorsque le formulaire est réduit dans une feuille de propriétés.
  
 **Pour obtenir une icône pour une classe de message sans activer le serveur de formulaires pour cette classe de message**
  
1. Appelez [la méthode IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) pour obtenir un pointeur vers une interface [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) . 
    
2. Appelez [la méthode IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) pour obtenir un pointeur vers une interface [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) . 
    
3. Appelez [la méthode IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) pour obtenir un handle d’icône. 
    
L’icône peut ensuite être affichée à l’aide des API Win32 standard.
  
> [!IMPORTANT]
> Une fois que vous avez l’icône d’une classe de message, veillez à mettre en cache cette icône. Le fait de ne pas mettre en cache les icônes affecte gravement les performances des applications clientes. Lors de la mise en cache des icônes, faites attention aux relations entre les classes de message et leurs sous-classes. Par exemple, si le IPM. Note.Meeting.Cancel message class happens to resolve back to IPM. Notez que ne supposez pas que toutes les sous-classes d’IPM. Notez que vous devez utiliser l’icône pour IPM. Remarque. 
  

