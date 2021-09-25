---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 69b371f5fda78159ff3626148cbc6ef32370a263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551351"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un objet fabrique de classes pour le formulaire.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Paramètres

 _clsidForm_
  
> [in] Identificateur de classe pour le formulaire à créer par la fabrique de classes.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppClassFactory_
  
> [out] Pointeur vers l’objet fabrique de classe.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet fabrique de classe a été renvoyé.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormFactory::CreateClassFactory** pour obtenir une fabrique de classes pour un formulaire spécifique. La fabrique de classes permet de créer des instances d’un formulaire qui gère les messages d’une classe spécifique et de contrôler l’accès à ces instances. 
  
La **méthode CreateClassFactory est** appelée par les visionneuses de formulaires pour obtenir un objet fabrique de classes pour les serveurs de formulaires qui implémentent plusieurs classes de message. Cette méthode reçoit un identificateur de classe (CLSID) en tant que paramètre. En fonction de ce paramètre, cette méthode peut déterminer le type spécifique d’objet usine de classe à renvoyer. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez retourner à partir de votre **implémentation CreateClassFactory** le même objet de fabrique de classe sur plusieurs appels pour le même identificateur de classe. La création d’une instance de fabrique de classe n’est pas obligatoire. 
  
Vous pouvez avoir une implémentation d’usine de classe unique qui crée des instances d’usine de classe appropriées à la demande, ou plusieurs implémentations d’usine de classe, une pour chaque classe de message.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

