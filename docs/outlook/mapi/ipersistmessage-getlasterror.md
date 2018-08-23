---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a39deb57a24b3a89ee10020a6442bcb1bca612a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575307"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Un type de données HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure [MAPIERROR](mapierror.md) retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si le formulaire ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Objets de formulaire implémentent la méthode de **IPersistMessage::GetLastError** pour fournir des informations relatives à un appel de méthode antérieurs ayant échoué. Visionneuses de formulaire peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données à partir de la structure [MAPIERROR](mapierror.md) dans une boîte de dialogue. 
  
Un appel à **GetLastError** n’affecte pas l’état du formulaire. **GetLastError** retourne le formulaire reste dans l’état dans lequel elle se trouvait avant l’appel a été effectué. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la structure **MAPIERROR** , si le formulaire fournit une, ce qui est indiqué par le paramètre _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, le formulaire ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, le formulaire retourne un pointeur null dans _lppMAPIError_ à la place. 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

