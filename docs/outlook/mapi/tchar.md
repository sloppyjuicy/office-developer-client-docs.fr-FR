---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787348"
---
# <a name="tchar"></a>TCHAR

  
  
**S’applique à**: Outlook 
  
Cha�ne de caract�res Win32 qui peut �tre utilis�e pour d�crire les cha�nes ANSI, DBCS ou Unicode. Pour les plateformes ANSI et DBCS, TCHAR est d�fini comme suit�:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Remarques

Pour les plateformes Unicode, TCHAR est d�fini comme synonyme du type WCHAR. 
  
Les clients MAPI peuvent utiliser le type de donn�es TCHAR pour repr�senter une cha�ne de type WCHAR ou CHAR. Veillez � bien d�finir la constante symbolique UNICODE et � limiter la plateforme lorsque cela est n�cessaire. MAPI interpr�te les informations de plateforme et traduit en interne les caract�res TCHAR dans la cha�ne appropri�e. Le type de propri�t� MAPI, PT_TSTRING, fonctionne comme le type de donn�es TCHAR. Lorsque la plateforme prend en charge le langage Unicode, le type PT_UNICODE est affect� aux propri�t�s de type PT_TSTRING lors de la compilation. Si la plateforme ne prend pas en charge le langage Unicode, ces propri�t�s ont le type PT_STRING8.
  
Pour plus d�informations sur cette fonctionnalit�, voir [Jeux de caract�res](mapi-character-sets.md) et [Liste de types de propri�t�s](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[Types de donn�es MAPI](mapi-data-types.md)

