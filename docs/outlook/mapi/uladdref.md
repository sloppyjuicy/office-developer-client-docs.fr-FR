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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787392"
---
# <a name="uladdref"></a>UlAddRef

  
  
**S’applique à**: Outlook 
  
Permet également d’appeler la méthode OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG UlAddRef(
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

 **UlAddRef** renvoie la valeur renvoyée par la méthode **IUnknown::AddRef** , qui est la nouvelle valeur du décompte de références pour l’interface. La valeur est différente de zéro. 
  
Pour plus d’informations sur **IUnknown::AddRef**, voir [implémentation de l’IUnknown Interface](implementing-the-iunknown-interface.md). 
  

