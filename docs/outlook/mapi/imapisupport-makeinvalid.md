---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0830efe7ef5b76f2f25aca86a7d737bdc0810a03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567430"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Marque un objet comme inutilisable.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _lpObject_
  
> [in] Pointeur vers l’objet à invalider. L’interface de l’objet doit être dérivée **d’IUnknown**.
    
 _ulRefCount_
  
> [in] Nombre de références présentes de l’objet.
    
 _cMethods_
  
> [in] Nombre de méthodes dans la table vtable de l’objet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet a été marqué comme inutilisable.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::MakeInvalid** est implémentée pour tous les objets de prise en charge. L’objet à invalider doit être dérivé de l’interface **IUnknown** ou d’une interface dérivée de **IUnknown**.
  
 **MakeInvalid** marque un objet comme inutilisable en remplaçant le vtable de l’objet par un vtable stub de taille similaire dans lequel les méthodes **IUnknown::AddRef** et **IUnknown::Release** s’exécutent comme prévu. Toutefois, toutes les autres méthodes échouent, renvoyant la valeur MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les fournisseurs de services et les services de messagerie **appellent généralement MakeInvalid** au moment de l’arrêt. Toutefois, **MakeInvalid** peut être appelé à tout moment. Par exemple, si un client libère un objet sans libérer certains de ses sous-objets, vous pouvez appeler **MakeInvalid** immédiatement pour libérer ces sous-objets. 
  
Vous devez posséder l’objet que vous tentez d’invalider. Elle doit avoir au moins 16 octets de long et avoir au moins trois méthodes dans sa table vtable. 
  
Vous pouvez appeler **MakeInvalid,** puis effectuer n’importe quel travail d’arrêt, par exemple ignorer les structures de données associées, généralement effectué lors de la libération d’un objet. Le code de prise en charge de l’objet n’a pas besoin d’être conservé en mémoire, car MAPI libère la mémoire en appelant [MAPIFreeBuffer,](mapifreebuffer.md) puis libère l’objet. Vous pouvez libérer des ressources, **appeler MakeInvalid,** puis ignorer l’objet invalidé. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

