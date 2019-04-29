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
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438630"
---
# <a name="displaying-form-icons"></a>Affichage des icônes de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l'affichage d'une liste de messages dans un dossier, il est utile pour vos utilisateurs de distinguer les messages avec des classes de message personnalisées du IPM standard. Notez les messages. Les classes de message personnalisées correspondent aux serveurs de formulaires et les serveurs de formulaires fournissent des icônes pour se représenter eux-mêmes. Vous pouvez afficher ces icônes dans la liste des messages pour alerter les utilisateurs de la classe de message de chaque message avant que l'utilisateur n'ouvre les messages. En règle générale, l'icône dans la propriété **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) du formulaire est celle qui doit être affichée dans la liste des messages. Les formulaires ont également une propriété **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) qui peut être affichée lorsque le formulaire est réduit dans une feuille de propriétés.
  
 **Pour obtenir une icône pour une classe de message sans activer le serveur de formulaires pour cette classe de message**
  
1. Appelez la méthode [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) pour obtenir un pointeur vers une interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) . 
    
2. Appelez la méthode [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) pour obtenir un pointeur vers une interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) . 
    
3. Appelez la méthode [IMAPIFormInfo:: MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) pour obtenir un descripteur d'icône. 
    
L'icône peut ensuite être affichée à l'aide des API Win32 standard.
  
> [!IMPORTANT]
> Une fois que vous avez l'icône d'une classe de message, efforcez-vous de mettre en cache cette icône. Aucune icône de mise en cache n'affecte gravement les performances des applications clientes. Lors de la mise en cache des icônes, soyez attentifs aux relations entre les classes de message et leurs sous-classes. Par exemple, si le IPM. Note. Meeting. Cancel la classe de message se trouve à nouveau résolu en IPM. Notez que vous ne devez pas supposer que toutes les sous-classes de IPM. Remarque doit utiliser l'icône de IPM. Note. 
  

