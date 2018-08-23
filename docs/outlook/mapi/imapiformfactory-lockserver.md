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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c4d7273b7393d421092bb06377aece0842b5fb67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590819"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Tenir à jour un serveur de formulaire ouvert en mémoire.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _fLockServer_
  
> [in] **true** pour augmenter le nombre de verrous ; Sinon, **false**.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormFactory::LockServer** pour conserver une application de serveur de formulaire ouvert en mémoire. Conserver le serveur du formulaire en mémoire améliore ses performances lorsque les formulaires sont souvent créés et publiés. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

La méthode **IMAPIFormFactory::LockServer** est très similaire à la méthode [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) . En fait, la méthode **IMAPIFormFactory::LockServer** gère un décompte de combien de fois qu’il a été appelé ; dans la mesure où ce nombre est supérieur à 0, la méthode empêche le serveur de formulaire déchargé de la mémoire. Vous pouvez utiliser la fonction [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) pour mettre en place. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

