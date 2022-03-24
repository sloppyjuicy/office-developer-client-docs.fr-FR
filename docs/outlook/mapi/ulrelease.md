---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96b35884a98312b0efb1d297481967ce6df1bb54
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720765"
---
# <a name="ulrelease"></a>UlRelease

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une autre méthode pour appeler la méthode OLE **IUnknown::Release**. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Paramètres

 _sous-groupe_
  
> [in] Pointeur vers une interface dérivée de l’interface **IUnknown** , en d’autres termes toute interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.
    
## <a name="remarks"></a>Remarques

Le nombre de références est le nombre de pointeurs existants vers l’objet à libérer. 
  
Si le  _paramètre de contrôle_ est NULL, la fonction renvoie immédiatement sans **appeler IUnknown::Release**
  
 **UlRelease renvoie** la valeur renvoyée par la méthode **IUnknown::Release** , qui peut être égale au nombre de références de l’objet à libérer. 
  
Pour plus d’informations **sur IUnknown::Release**, voir [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  

