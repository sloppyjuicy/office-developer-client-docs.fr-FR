---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 82d2d52ef2685d520af7996e685d6e894e1e0099
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462367"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations de configuration d’impression de l’objet de formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> Masque de bits d’indicateurs qui contrôle le type des chaînes. L’indicateur suivant peut être utilisé :
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **hDevmode**
  
> Handle vers le mode de l’imprimante.
    
 **hDevnames**
  
> Handle vers le chemin d’accès de l’imprimante.
    
 **ulFirstPageNumber**
  
> Numéro de page de la première page à imprimer.
    
 **ulFPrintAttachments**
  
> Indicateur qui indique s’il existe des pièces jointes à imprimer. S’il existe des pièces jointes à imprimer, le membre **ulFPrintAttachments** est définie sur 1. S’il n’existe aucune pièce jointe à imprimer, elle est définie sur 0. 
    
## <a name="remarks"></a>Remarques

La structure **FORMPRINTSETUP** est utilisée pour décrire les informations de configuration d’impression d’un objet de formulaire. Les implémentations de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) remplissent la structure **FORMPRINTSETUP** et la retournent dans le contenu du paramètre  _de sortie lppFormPrintSetup_ de **GetPrintSetup**.
  
Si l’indicateur MAPI_UNICODE est transmis dans le paramètre _ulFlags_ de **GetPrintSetup**, les chaînes référencés par les membres **hDevmode** et **hDevnames** doivent être au format Unicode. Dans le cas contraire, les chaînes doivent être au format ANSI. 
  
Les visionneuses de formulaires implémentant **IMAPIViewContext** doivent allouer la structure **FORMPRINTSETUP** à l’aide de la fonction [d’allocation MAPIAllocateBuffer](mapiallocatebuffer.md), mais allouer les membres individuels, **hDevMode** et **hDevNames**, avec la fonction Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110). La libération de mémoire est gérée de la même manière. Les membres **hDevMode** et **hDevNames** doivent être libérés à l’aide de la fonction Windows [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108), tandis que la structure **FORMPRINTSETUP** doit être libérée avec la fonction [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Structures MAPI](mapi-structures.md)

