---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e1da4bca0307e69c36b9d8db2ee43be2c664aafc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614100"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la page de code d'Transport-Neutral flux TNEF (Encapsulation Format).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tnef.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Paramètres

 _lpStream_
  
> [in] Pointeur vers une interface OLE **IStream** d’objet de flux de stockage fournissant une source pour un message de flux TNEF. 
    
 _lpulCodepage_
  
> [out] Pointeur vers la page de code du flux.
    
 _lpulSubCodepage_
  
> [out] Pointeur vers la page de sous-code du flux.
    
## <a name="return-value"></a>Valeur renvoyée

 **S_OK**
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Une erreur s’est produite lors de la lecture d’un attribut dans le flux TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> Le flux n’était pas un flux TNEF ou une erreur s’est produite lors de la lecture de l’attribut attOemCodepage.
    
## <a name="remarks"></a>Remarques

Utilisez la **fonction GetTnefStreamCodepage** pour lire l’attribut **attOemCodepage** du flux TNEF afin de déterminer la page de code et la page de sous-code. Si **attOemCodepage** est in found, **GetTnefStreamCodepage** renvoie une page de code 437 et une page de sous-code de 0. 
  
## <a name="see-also"></a>Voir aussi



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

