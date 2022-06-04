---
title: UlRelease
description: Décrit UlRelease, notamment comment il fournit une autre façon d’appeler la méthode OLE IUnknown::Release.
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
ms.openlocfilehash: 4350b0bb3d440ea9a0d41d59de9090f003d64c78
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894410"
---
# <a name="ulrelease"></a>UlRelease

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une autre façon d’appeler la méthode OLE **IUnknown::Release**. 
  
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

 _Punk_
  
> [in] Pointeur vers une interface dérivée de l’interface **IUnknown** , c’est-à-dire toute interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

Le nombre de références est le nombre de pointeurs existants vers l’objet à libérer. 
  
Si le paramètre  _punk_ est NULL, la fonction retourne immédiatement sans appeler **IUnknown::Release**
  
 **UlRelease** retourne la valeur retournée par la méthode **IUnknown::Release** , qui peut être égale au nombre de références pour l’objet à libérer. 
  
Pour plus d’informations sur **IUnknown::Release**, consultez [Implémentation de l’interface IUnknown](implementing-the-iunknown-interface.md). 
  

