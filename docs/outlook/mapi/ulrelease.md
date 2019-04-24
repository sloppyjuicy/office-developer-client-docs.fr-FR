---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315294"
---
# <a name="ulrelease"></a>UlRelease

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Offre un autre moyen d'appeler la méthode OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Paramètres

 _Punk_
  
> dans Pointeur vers une interface dérivée de l'interface **IUnknown** , en d'autres termes, toute interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.
    
## <a name="remarks"></a>Remarques

Le nombre de références est le nombre de pointeurs existants vers l'objet à libérer. 
  
Si le paramètre _punk_ est null, la fonction renvoie immédiatement sans appeler **IUnknown:: Release**
  
 **UlRelease** renvoie la valeur retournée par la méthode **IUnknown:: Release** , qui peut être égale au nombre de références pour l'objet à libérer. 
  
Pour plus d'informations sur **IUnknown:: Release**, consultez [la rubrique Implementing the IUnknown interface](implementing-the-iunknown-interface.md). 
  

