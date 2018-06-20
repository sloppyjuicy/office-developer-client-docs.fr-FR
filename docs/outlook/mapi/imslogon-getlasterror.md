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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784313"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**S’applique à**: Outlook 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite lors de l’objet de la banque de message. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Un type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent pour l’objet de banque de messages.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucun **MAPIERROR** pour renvoyer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMSLogon::GetLastError** pour récupérer des informations à afficher dans un message à l’utilisateur concernant la dernière erreur renvoyée par un appel de méthode pour l’objet de banque de messages. 
  
Pour libérer la mémoire allouée par MAPI pour la structure **MAPIERROR** retournée, les applications clientes ont besoin d’appeler la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement. 
  
La valeur renvoyée par **GetLastError** doit être S_OK d’une application pour utiliser le **MAPIERROR**. Même si la valeur de retour est S_OK, un **MAPIERROR** ne peut pas être retourné. Si l’implémentation ne peut pas déterminer quelle était la dernière erreur, ou si une **MAPIERROR** n’est pas disponible pour que l’erreur, **GetLastError** retourne un pointeur vers NULL dans _lppMAPIError_ à la place. 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

