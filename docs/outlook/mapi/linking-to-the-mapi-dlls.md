---
title: Liaison aux DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784511"
---
# <a name="linking-to-the-mapi-dlls"></a>Liaison aux DLL MAPI

  
  
**S’applique à**: Outlook 
  
Clients MAPI peuvent lier aux DLL MAPI implicite ou explicite en utilisant les fonctions Windows **LoadLibrary** et **GetProcAddress**. Pour plus d’informations sur la liaison explicitement DLL MAPI, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md).
  
MAPI fournit des instructions de définition de type dans le MAPIX. Fichier d’en-tête H pour chacune des fonctions suivantes :
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[Exécuter MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Utilisez ces définitions de type à appeler correctement les points d’entrée correspondante si la liaison explicitement les DLL MAPI.
  
Fournisseurs de services peuvent contenir des fonctionnalités non MAPI — fonctionnalités qui ne sont pas complètement liées à MAPI — dans leur DLL. Si vous avez besoin d’utiliser ces fonctionnalités, appeler **LoadLibrary** avant d’utiliser la DLL et **FreeLibrary** pour supprimer la DLL de la mémoire après son utilisation. MAPI n’a pas connaissance d’utilisations non MAPI d’un fournisseur de service DLL, il n’aucune garantie que la DLL sera disponible lorsqu’elle est nécessaire. MAPI libère un fournisseur de services DLL quand il y a plus aucun tous les clients avec des sessions actives nécessitant ses services. 
  

