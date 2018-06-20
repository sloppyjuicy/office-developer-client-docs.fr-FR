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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783925"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**S’applique à**: Outlook 
  
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

