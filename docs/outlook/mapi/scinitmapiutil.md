---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787070"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**S’applique à**: Outlook 
  
Remplace les [exécuter MAPIInitialize](mapiinitialize.md) si uniquement les fonctions d’utilitaire select sont utilisées. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) coopèrent pour appeler et sélectionnez utilitaire, par opposition à [exécuter MAPIInitialize](mapiinitialize.md)qui appelle principaux, ainsi que des utilitaires fonctions de publication. Lorsque **ScInitMapiUtil** appelle les fonctions utilitaires, il initialise également la mémoire nécessaire. 
  
Lors de l’utilisation des fonctions **ScInitMapiUtil** a appelée est terminée, **DeinitMapiUtil** doit être explicitement appelée pour libérer les. En revanche, **exécuter MAPIInitialize** appelle implicitement **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUninitialize](mapiuninitialize.md)

