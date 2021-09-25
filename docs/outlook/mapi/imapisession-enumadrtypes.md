---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 590f965d1e2e1155f3171f0888efda7613d4830e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592458"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format des types d’adresses renvoyés. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les types d’adresses sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les types d’adresses sont au format ANSI.
    
 _lpcAdrTypes_
  
> [out] Pointeur vers un nombre de types d’adresses pointés par le _paramètre lpppszAdrTypes._ 
    
 _lpppszAdrTypes_
  
> [out] Pointeur vers un tableau de pointeurs vers des types d’adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les types d’adresses ont été récupérés avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::EnumAdrTypes** renvoie une liste des types d’adresses qui peuvent être gérés par tous les fournisseurs de transport actifs dans la session. Les types d’adresses pour les fournisseurs de transport qui ne sont pas actuellement chargés ne sont pas inclus dans la liste. Les fournisseurs de transport s’inscrivent pour gérer un ou plusieurs types d’adresses lorsque MAPI appelle leur méthode [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez [MAPIFreeBuffer pour](mapifreebuffer.md) libérer le tableau de chaînes pointé par _le paramètre lpppszAdrTypes._ 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

