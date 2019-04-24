---
title: Allocation et libération de mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281584"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Allocation et libération de mémoire dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
En plus de spécifier comment allouer et libérer de la mémoire, MAPI définit un modèle pour savoir quand la mémoire passée entre la méthode d'interface publique et les appels de fonction d'API doit être libérée. Le modèle s'applique uniquement à la mémoire allouée pour les paramètres qui ne sont pas des pointeurs vers des interfaces, comme des chaînes et des pointeurs vers des structures. Les pointeurs d'interface utilisent le mécanisme de décompte de références implémenté via **IUnknown**. Lors de l'allocation et de la libération de mémoire non-MAPI en interne au sein d'une application client ou d'un fournisseur de services, utilisez le mécanisme approprié. 
  
Le modèle définit les paramètres de l'un des trois types suivants. Il peut s'agir de paramètres d'entrée, définis par l'appelant avec des informations à utiliser par la fonction appelée ou la méthode appelée, les paramètres de sortie, définis par la fonction ou la méthode appelée et renvoyés à l'appelant ou les paramètres d'entrée-sortie, une combinaison des deux types. Les paramètres de sortie sont fréquemment des pointeurs vers des données ou des pointeurs vers des pointeurs vers des données. Bien que la fonction appelée soit chargée d'allouer les données pour les paramètres de sortie, l'appelant alloue la mémoire pour le pointeur. 
  
Les règles d'allocation et de libération de mémoire pour ces types de paramètres sont expliquées dans le tableau suivant.
  
|**Type**|**Allocation de mémoire**|**Version de mémoire**|
|:-----|:-----|:-----|
|Input  <br/> |L'appelant est responsable et peut utiliser n'importe quel mécanisme.  <br/> |L'appelant est responsable et peut utiliser n'importe quel mécanisme.  <br/> |
|Output  <br/> |La fonction appelée est responsable et doit utiliser **MAPIAllocateBuffer**. Pour plus d'informations, consultez la rubrique [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |L'appelant est responsable et doit utiliser **MAPIFreeBuffer**. Pour plus d'informations, consultez la rubrique [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Entrée/sortie  <br/> |L'appelant est responsable de l'allocation initiale et la fonction appelée peut être réaffectée, si nécessaire, à l'aide de **MAPIAllocateBuffer**.  <br/> |La fonction appelée est responsable de la libération initiale si la réallocation est nécessaire. L'appelant doit libérer la valeur de retour finale.  <br/> |
   
En cas de défaillance, les responsables des méthodes d'interface doivent être attentifs aux paramètres de sortie et d'entrée en sortie, car l'appelant n'a généralement aucun moyen de les nettoyer. Si une erreur est renvoyée, chaque paramètre de sortie ou d'entrée doit être conservé à la valeur initialisée par l'appelant ou défini sur une valeur qui peut être nettoyée sans aucune action de la part de l'appelant. Par exemple, un pointeur de sortie-paramètre `void ** ppv` de doit être conservé tel qu'il était sur entrée ou peut être défini sur `*ppv = NULL`null ().
  

