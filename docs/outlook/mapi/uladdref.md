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
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432834"
---
# <a name="uladdref"></a>UlAddRef

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une autre méthode pour appeler la méthode OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Paramètres

 _sous-président_
  
> [in] Pointeur vers une interface dérivée de l’interface **IUnknown,** en d’autres termes toute interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.
    
## <a name="remarks"></a>Remarques

 **UlAddRef renvoie** la valeur renvoyée par la méthode **IUnknown::AddRef,** qui est la nouvelle valeur du nombre de références pour l’interface. La valeur est non zéro. 
  
Pour plus d’informations **sur IUnknown::AddRef**, voir [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  

