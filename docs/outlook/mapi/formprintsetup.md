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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 83194b47faf7892d5da568a354921511eb097210
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582951"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit les informations de configuration de l’impression de l’objet de formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
   
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

## <a name="members"></a>Members

 **ulFlags**
  
> Masque de bits d’indicateurs qui contrôle le type des chaînes. L’indicateur suivantes peut être utilisées :
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **hDevmode**
  
> Handle vers le mode de l’imprimante.
    
 **hDevnames**
  
> Gérer le chemin d’accès de l’imprimante.
    
 **ulFirstPageNumber**
  
> Numéro de page de la première page à imprimer.
    
 **ulFPrintAttachments**
  
> Indicateur qui indique s’il existe des pièces jointes à imprimer. S’il existe des pièces jointes à imprimer, le membre **ulFPrintAttachments** est défini sur 1. S’il n’y a pas de pièces jointes à imprimer, elle est définie sur 0. 
    
## <a name="remarks"></a>Remarques

La structure **FORMPRINTSETUP** est utilisée pour décrire les informations de configuration de l’impression d’un objet de formulaire. Les implémentations de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) remplir la structure **FORMPRINTSETUP** et retourner dans le contenu du paramètre de sortie _lppFormPrintSetup_ de **GetPrintSetup**.
  
Si l’indicateur MAPI_UNICODE est passé dans le paramètre _ulFlags_ de **GetPrintSetup**, les chaînes référencées par les membres **hDevmode** et **hDevnames** doivent être au format Unicode. Dans le cas contraire, les chaînes doivent être au format ANSI. 
  
Visionneuses de formulaire l’implémentation **IMAPIViewContext** doivent affecter la structure **FORMPRINTSETUP** à l’aide de la fonction d’allocation MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), mais allouer les membres individuels, **hDevMode** et **hDevNames**, avec la fonction Windows [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110). La version de la mémoire est gérée de la même manière. Les membres **hDevMode** et **hDevNames** doivent être libérés à l’aide de la fonction Windows [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) tandis que la structure **FORMPRINTSETUP** doit être libérée avec la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Structures MAPI](mapi-structures.md)

