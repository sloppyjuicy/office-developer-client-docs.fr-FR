---
title: Liaison aux fichiers DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270041"
---
# <a name="linking-to-the-mapi-dlls"></a>Liaison aux fichiers DLL MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients MAPI peuvent établir des liens vers les dll MAPI de manière implicite ou explicitement à l'aide des fonctions Windows **LoadLibrary** et **GetProcAddress**. Pour plus d'informations sur la liaison explicite des dll MAPI, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md).
  
MAPI fournit des instructions de définition de type dans le MAPIX. H pour chacune des fonctions suivantes:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Utilisez ces définitions de types pour appeler correctement les points d'entrée correspondants si vous liez explicitement les dll MAPI.
  
Les fournisseurs de services peuvent contenir des fonctionnalités non MAPI (fonctionnalités totalement non liées à MAPI) dans leur DLL. Si vous devez utiliser ces fonctionnalités, appelez **LoadLibrary** avant d'utiliser la dll et **FreeLibrary** pour supprimer la dll de la mémoire après son utilisation. Comme MAPI n'est pas conscient des utilisations non-MAPI d'un fournisseur de services DLL, il n'existe aucune garantie que la DLL sera disponible si nécessaire. MAPI publie une DLL de fournisseur de services lorsqu'il n'y a plus de client avec des sessions actives qui nécessitent ses services. 
  

