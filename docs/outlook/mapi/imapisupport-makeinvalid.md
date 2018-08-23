---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570736"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Marque un objet comme étant inutilisable.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _lpObject_
  
> [in] Pointeur vers l’objet est invalidé. Interface de l’objet doit être dérivée de **IUnknown**.
    
 _ulRefCount_
  
> [in] Décompte de références présente de l’objet.
    
 _cMethods_
  
> [in] Le nombre des méthodes dans vtable de l’objet.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’objet a été marqué comme inutilisable.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::MakeInvalid** est implémentée pour tous les objets de prise en charge. L’objet est invalidé doit être dérivée à partir de l’interface **IUnknown** ou d’une interface dérivée de **IUnknown**.
  
 **MakeInvalid** marque un objet comme étant inutilisable en remplaçant vtable de l’objet par une vtable stub de taille similaire dans lequel les méthodes **IUnknown::AddRef** and **IUnknown::Release** fonctionnent comme prévu. Toutefois, toutes les autres méthodes échouent, retourner la valeur MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Fournisseurs de services et les services de messagerie généralement appellent **MakeInvalid** au moment de l’arrêt. Toutefois, **MakeInvalid** peut être appelée à tout moment. Par exemple, si un client libère un objet sans relâcher certains de ses sous-objets, vous pouvez appeler **MakeInvalid** immédiatement pour libérer les sous-objets. 
  
Vous devez posséder l’objet que vous essayez d’invalider. Elle doit être d’au moins 16 octets et avoir au moins trois méthodes dans sa table vtable. 
  
Vous pouvez appeler **MakeInvalid** et puis effectuer n’importe quel l’arrêt, par exemple en supprimant les structures de données associées, qui est généralement effectuée lors de la publication d’un objet. Code pour prendre en charge l’objet pas conserver en mémoire, car MAPI libère de la mémoire en appelant [MAPIFreeBuffer](mapifreebuffer.md) , puis libère l’objet. Vous pourrez libérer les ressources, appelez **MakeInvalid**et puis ignorer l’objet non valide. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

