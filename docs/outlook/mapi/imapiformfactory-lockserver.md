---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
ms.openlocfilehash: 5a12ac16eea69fc74824fead40ccc80fb487892a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372275"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Conserve un serveur de formulaire ouvert en mémoire.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _fLockServer_
  
> [in] **true** pour incrémenter le nombre de verrous ; sinon, **false**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent **la méthode IMAPIFormFactory::LockServer** pour conserver une application serveur de formulaire ouverte en mémoire. La conservation du serveur de formulaires en mémoire améliore ses performances lorsque les formulaires sont fréquemment créés et libérés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La **méthode IMAPIFormFactory::LockServer** est très similaire à la [méthode IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) . En fait, la **méthode IMAPIFormFactory::LockServer** conserve le nombre de fois qu’elle a été appelée ; Tant que ce nombre est supérieur à 0, la méthode empêche le serveur de formulaires d’être déchargé de la mémoire. Vous pouvez utiliser la [fonction CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) pour implémenter cela. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

