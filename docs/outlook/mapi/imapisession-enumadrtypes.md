---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439288"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Renvoie les types d'adresses qui peuvent être gérées par tous les fournisseurs de transport dans la session. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de réindicateur qui indique le format des types d'adresses renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les types d'adresses sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les types d'adresses sont au format ANSI.
    
 _lpcAdrTypes_
  
> remarquer Pointeur vers le nombre de types d'adresses vers lequel pointe le paramètre _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> remarquer Pointeur vers un tableau de pointeurs vers des types d'adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les types d'adresses ont été récupérés avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: EnumAdrTypes** renvoie la liste des types d'adresses qui peuvent être gérées par tous les fournisseurs de transport actifs dans la session. Les types d'adresses pour les fournisseurs de transport qui ne sont pas actuellement chargés ne sont pas inclus dans la liste. Les fournisseurs de transport s'inscrivent pour gérer un ou plusieurs types d'adresses lorsque MAPI appelle la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de chaînes désigné par le paramètre _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

