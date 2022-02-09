---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e0ea3adad5ed1dfc0fc2bed7b2ec162b22a6bc22
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462630"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour l’objet de la boutique de messages. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent pour l’objet de magasin de messages.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être paramétré sur NULL s’il n’existe **aucun MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Utilisez **la méthode IMSLogon::GetLastError** pour récupérer les informations à afficher dans un message à l’utilisateur concernant la dernière erreur renvoyée par un appel de méthode pour l’objet de magasin de messages. 
  
Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR** renvoyée, les applications clientes doivent appeler uniquement la [fonction MAPIFreeBuffer](mapifreebuffer.md) . 
  
La valeur de retour **de GetLastError** doit être S_OK pour qu’une application utilise **MAPIERROR**. Même si la valeur renvoyée est S_OK, il se peut **qu’un MAPIERROR** ne soit pas renvoyé. Si l’implémentation ne peut pas déterminer la dernière erreur ou si **un MAPIERROR** n’est pas disponible pour cette erreur, **GetLastError** renvoie un pointeur vers NULL dans  _lppMAPIError_ à la place. 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

