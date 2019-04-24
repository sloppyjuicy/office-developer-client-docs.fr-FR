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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342174"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> dans Identificateur de classe du formulaire à créer par la fabrique de classes.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppClassFactory_
  
> remarquer Pointeur vers l'objet de fabrique de classes.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet de fabrique de classe a été renvoyé.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormFactory:: CreateClassFactory** pour obtenir une fabrique de classe pour un formulaire spécifique. La fabrique de classe est utilisée pour créer des instances d'un formulaire qui gère les messages d'une classe spécifique et pour contrôler l'accès à ces instances. 
  
La méthode **CreateClassFactory** est appelée par les visionneuses de formulaire pour obtenir un objet de fabrique de classe pour les serveurs de formulaires qui implémentent plusieurs classes de message. Cette méthode reçoit un identificateur de classe (CLSID) en tant que paramètre. En fonction de ce paramètre, cette méthode peut déterminer le type spécifique de l'objet Factory de classe à renvoyer. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez revenir de votre implémentation **CreateClassFactory** le même objet de fabrique de classes sur plusieurs appels pour le même identificateur de classe. La création d'une nouvelle instance de fabrique de classes n'est pas obligatoire. 
  
Vous pouvez avoir une seule implémentation de fabrique de classe qui crée des instances de fabrique de classe appropriées sur demande ou plusieurs implémentations de fabrique de classe, une pour chaque classe de message.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

