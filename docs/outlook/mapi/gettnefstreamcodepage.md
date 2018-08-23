---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d00a2ce3ebec24ca69875bdcb83066d8b891137a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585954"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détermine la page de codes pour un flux de Transport-Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes et des fournisseurs de services.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Paramètres

 _lpStream_
  
> [in] Pointeur vers une flux de données de stockage objet interface OLE **IStream** fournissant une source d’un message de flux TNEF. 
    
 _lpulCodepage_
  
> [out] Pointeur vers la page de code de l’objet stream.
    
 _lpulSubCodepage_
  
> [out] Pointeur vers la page subcode du flux.
    
## <a name="return-value"></a>Valeur renvoy�e

 **S_OK**
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Une erreur de lecture d’un attribut dans le flux TNEF est survenu.
    
 **MAPI_E_CORRUPT_DATA**
  
> Le flux n’était pas un flux TNEF ou il s’est produit une erreur de lecture de l’attribut attOemCodepage.
    
## <a name="remarks"></a>Remarques

Utilisez la fonction **GetTnefStreamCodepage** pour lire l’attribut **attOemCodepage** de l’objet stream TNEF pour déterminer la page de code et la page subcode. Si **attOemCodepage** est introuvable, **GetTnefStreamCodepage** renvoie une page de codes de 437 et une page subcode 0. 
  
## <a name="see-also"></a>Voir aussi



[attOemCodepage](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

