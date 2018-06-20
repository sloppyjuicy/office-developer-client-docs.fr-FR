---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783793"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**S’applique à**: Outlook 
  
Renvoie un objet de fabrique de classe pour le formulaire.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Paramètres

 _clsidForm_
  
> [in] Un identificateur de classe pour le formulaire doit être créé à la fabrique de classe.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppClassFactory_
  
> [out] Pointeur vers l’objet de fabrique de classe.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’objet de fabrique de classe a été retournée.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormFactory::CreateClassFactory** pour obtenir une fabrique de classe pour un formulaire spécifique. La fabrique de classe est utilisée pour créer des instances d’un formulaire qui gère les messages d’une classe spécifique et pour contrôler l’accès à ces instances. 
  
La méthode **CreateClassFactory** est appelée par les visionneuses de formulaire pour obtenir un objet de fabrique de classe pour les serveurs de formulaire qui implémentent plusieurs classes de message. Cette méthode reçoit un identificateur de classe (CLSID) en tant que paramètre. En fonction de ce paramètre, cette méthode peut déterminer le type spécifique de l’objet de fabrique de classe à renvoyer. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous pouvez renvoyer à partir de votre implémentation **CreateClassFactory** le même objet de fabrique de classe sur plusieurs appels pour le même identificateur de classe. Création d’une nouvelle instance de fabrique de classe n’est pas obligatoire. 
  
Vous pouvez avoir une implémentation de fabrique de classe unique qui crée des instances de fabrique de classe appropriée à la demande ou de plusieurs implémentations de fabrique de classe, un pour chaque classe de message.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

