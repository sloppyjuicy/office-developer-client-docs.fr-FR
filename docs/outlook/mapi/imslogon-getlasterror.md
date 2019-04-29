---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425875"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur survenue pour l'objet de banque de messages. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Un type de données HRESULT qui contient la valeur d'erreur générée dans l'appel de méthode précédent pour l'objet de banque de messages.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null s'il n'y a pas de **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMSLogon:: GetLastError** pour extraire les informations à afficher dans un message à l'utilisateur concernant la dernière erreur renvoyée par un appel de méthode pour l'objet de banque de messages. 
  
Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR** renvoyée, les applications clientes doivent appeler uniquement la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
La valeur renvoyée par **GetLastError** doit être S_OK pour qu'une application utilise **MAPIERROR**. Même si la valeur renvoyée est S_OK, il se peut qu'un **MAPIERROR** ne soit pas retourné. Si l'implémentation ne peut pas déterminer la dernière erreur ou si un **MAPIERROR** n'est pas disponible pour cette erreur, **GetLastError** renvoie un pointeur vers une valeur null dans _lppMAPIError_ à la place. 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

