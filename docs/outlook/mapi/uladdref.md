---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592371"
---
# <a name="uladdref"></a>UlAddRef

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet également d’appeler la méthode OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Paramètres

 _pUnk_
  
> [in] Pointeur vers une interface dérivé de l’interface **IUnknown** , en d’autres termes n’importe quelle interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

 **UlAddRef** renvoie la valeur renvoyée par la méthode **IUnknown::AddRef** , qui est la nouvelle valeur du décompte de références pour l’interface. La valeur est différente de zéro. 
  
Pour plus d’informations sur **IUnknown::AddRef**, voir [implémentation de l’IUnknown Interface](implementing-the-iunknown-interface.md). 
  

