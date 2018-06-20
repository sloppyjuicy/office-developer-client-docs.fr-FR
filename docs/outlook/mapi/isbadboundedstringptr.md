---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784448"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**S’applique à**: Outlook 
  
Vérifie que le processus appelant dispose d’un accès en lecture à la plage spécifiée de la mémoire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiwin.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes et des fournisseurs de services.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers une chaîne ASCII.
    
 _cchMax_
  
> [in] La taille maximale de la chaîne de caractères. La fonction vérifie l’accès en lecture dans tous les caractères jusqu'à le caractère null de fin de la chaîne, ou le nombre de caractères spécifié par ce paramètre, la plus petite. Si ce paramètre est zéro, la valeur de retour est égale à zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

La valeur de retour est égale à zéro lorsque le processus d’appel a accès en lecture à tous les caractères jusqu'à le caractère null de fin de la chaîne ou le nombre de caractères spécifié par _cchMax_un accès en lecture.
  
La valeur de retour est différent de zéro lorsque le processus appelant ne dispose pas d’un accès en lecture à tous les caractères jusqu'à le caractère null de fin de la chaîne ou le nombre de caractères spécifié par _cchMax_un accès en lecture.
  
## <a name="remarks"></a>Remarques

La fonction **IsBadBoundedStringPtr** est équivalente à l’aide de **IsBadStringPtr**.
  
## <a name="see-also"></a>Voir aussi



[IsBadStringPtr](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

