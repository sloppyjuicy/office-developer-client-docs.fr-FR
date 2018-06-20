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
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787414"
---
# <a name="ulrelease"></a>UlRelease

  
  
**S’applique à**: Outlook 
  
Permet également d’appeler la méthode OLE **IUnknown::Release**. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Paramètres

 _pUnk_
  
> [in] Pointeur vers une interface dérivé de l’interface **IUnknown** , en d’autres termes n’importe quelle interface MAPI. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

Le décompte de références est le nombre de pointeurs existants à l’objet doit être publié. 
  
Si le paramètre _punk_ est NULL, la fonction retourne immédiatement sans appeler **IUnknown::Release**
  
 **UlRelease** renvoie la valeur renvoyée par la méthode **IUnknown::Release** , qui peut être égale au nombre de références de l’objet doit être publié. 
  
Pour plus d’informations sur **IUnknown::Release**, voir [implémentation de l’IUnknown Interface](implementing-the-iunknown-interface.md). 
  

