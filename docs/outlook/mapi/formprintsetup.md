---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327285"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations de configuration d'impression de l'objet Form. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
   
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
  
> Masque de des indicateurs qui contrôle le type des chaînes. L'indicateur suivant peut être utilisé:
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 **hDevmode**
  
> Gérer le mode de l'imprimante.
    
 **hDevnames**
  
> Handle vers le chemin d'accès de l'imprimante.
    
 **ulFirstPageNumber**
  
> Numéro de page de la première page à imprimer.
    
 **ulFPrintAttachments**
  
> Indicateur qui indique s'il existe des pièces jointes à imprimer. S'il y a des pièces jointes à imprimer, le membre **ulFPrintAttachments** est défini sur 1. S'il n'y a pas de pièces jointes à imprimer, il est défini sur 0. 
    
## <a name="remarks"></a>Remarques

La structure **FORMPRINTSETUP** est utilisée pour décrire les informations de configuration d'impression d'un objet Form. Implémentations de [IMAPIViewContext:: GetPrintSetup](imapiviewcontext-getprintsetup.md) renseignez la structure **FORMPRINTSETUP** et renvoyez-la dans le contenu du paramètre de sortie _lppFormPrintSetup_ de **GetPrintSetup**.
  
Si l'indicateur MAPI_UNICODE est transmis dans le paramètre _ulFlags_ de **GetPrintSetup**, les chaînes référencées par les membres **hDevmode** et **hDevnames** doivent être au format Unicode. Dans le cas contraire, les chaînes doivent être au format ANSI. 
  
Les visionneuses de formulaire implémentant **IMAPIViewContext** doivent allouer la structure **FORMPRINTSETUP** à l'aide de la fonction d'allocateur MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), mais allouer les membres individuels, **hDevMode** et **hDevNames**, avec la fonction de Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110). La version de la mémoire est gérée de la même manière. Les membres **hDevMode** et **hDevNames** doivent être libérés à l'aide de la fonction Windows [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) que la structure **FORMPRINTSETUP** doit être libérée avec la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Structures MAPI](mapi-structures.md)

