---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342139"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Conserve un serveur de formulaires ouvert en mémoire.
  
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
  
> dans **true** pour incrémenter le nombre de verrous; Sinon, **false**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormFactory:: LockServer** pour conserver une application Open Form Server en mémoire. Le fait de maintenir le serveur de formulaires en mémoire améliore ses performances lorsque les formulaires sont fréquemment créés et publiés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La méthode **IMAPIFormFactory:: LockServer** est très similaire à la méthode [IClassFactory:: LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) . Fondamentalement, la méthode **IMAPIFormFactory:: LockServer** conserve le nombre de fois qu'elle a été appelée; tant que ce nombre est supérieur à 0, la méthode empêche le serveur de formulaires d'être déchargé de la mémoire. Vous pouvez utiliser la fonction [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) pour l'implémenter. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

