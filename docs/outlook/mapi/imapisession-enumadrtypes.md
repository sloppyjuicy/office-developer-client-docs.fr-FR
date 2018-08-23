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
ms.openlocfilehash: 050068b542616d1ad4d133b289aba46db2888519
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587816"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Déconseillé. Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format pour les types d’adresse retournée. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les types d’adresses sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les types d’adresses sont au format ANSI.
    
 _lpcAdrTypes_
  
> [out] Un pointeur vers un nombre de types d’adresses indiqué par le paramètre _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> [out] Pointeur vers un tableau de pointeurs vers des types d’adresses.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les types d’adresses ont été récupérés correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::EnumAdrTypes** renvoie une liste des types d’adresses qui peuvent être gérés par tous les fournisseurs de transport actif dans la session. Les types d’adresses pour les fournisseurs de transport qui ne sont pas actuellement chargés ne sont pas inclus dans la liste. Fournisseurs de transport enregistrement pour gérer un ou plusieurs types d’adresses lors de leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) des appels MAPI. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de chaînes désigné par le paramètre _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

