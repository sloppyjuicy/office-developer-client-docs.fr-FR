---
title: Allocation et libération de mémoire dans MAPI
description: Décrit comment allouer et libérer de la mémoire dans MAPI en suivant les règles des paramètres d’entrée, des paramètres de sortie ou des paramètres de sortie d’entrée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
ms.openlocfilehash: 940cbe5bb261d3fcf28143d04cf9ceed5401434b
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770914"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Allocation et libération de mémoire dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016
  
En plus de spécifier comment allouer et libérer de la mémoire, MAPI définit un modèle permettant de savoir quand la mémoire transmise entre la méthode d’interface publique et les appels de fonction API doit être libérée. Le modèle s’applique uniquement à la mémoire allouée pour les paramètres qui ne sont pas des pointeurs vers des interfaces, telles que des chaînes et des pointeurs vers des structures. Les pointeurs d’interface utilisent le mécanisme de comptage des références implémenté via **IUnknown**. Lorsque vous allouez et libérez de la mémoire non liée à MAPI en interne au sein d’une application cliente ou d’un fournisseur de services, utilisez n’importe quel mécanisme logique.
  
Le modèle définit les paramètres comme l’un des trois types. Il peut s’agir de paramètres d’entrée, définis par l’appelant avec des informations à utiliser par la fonction ou la méthode appelée, des paramètres de sortie, définis par la fonction ou la méthode appelée et renvoyés à l’appelant, ou paramètres de sortie d’entrée, une combinaison des deux types. Les paramètres de sortie sont souvent des pointeurs vers des données ou des pointeurs vers des données. Bien que la fonction appelée soit responsable de l’allocation des données pour les paramètres de sortie, l’appelant alloue la mémoire pour le pointeur.
  
Les règles d’allocation et de libération de mémoire pour ces types de paramètres sont expliquées dans le tableau suivant.
  
|**Type (Type)**|**Allocation de mémoire**|**Version de la mémoire**|
|:-----|:-----|:-----|
|Input  <br/> |L’appelant est responsable et peut utiliser n’importe quel mécanisme. |L’appelant est responsable et peut utiliser n’importe quel mécanisme. |
|Sortie  <br/> |La fonction appelée est responsable et doit utiliser **MAPIAllocateBuffer**. Pour plus d’informations, consultez [MAPIAllocateBuffer](mapiallocatebuffer.md). |L’appelant est responsable et doit utiliser **MAPIFreeBuffer**. Pour plus d’informations, consultez [MAPIFreeBuffer](mapifreebuffer.md). |
|Sortie d’entrée  <br/> |L’appelant est responsable de l’allocation initiale et la fonction appelée peut se réallouer si nécessaire à l’aide de **MAPIAllocateBuffer**. |La fonction appelée est responsable de la libération initiale si la réallocation est nécessaire. L’appelant doit libérer la valeur de retour finale. |

En cas d’échec, les implémenteurs de méthodes d’interface doivent prêter attention aux paramètres de sortie et de sortie d’entrée, car l’appelant n’a généralement aucun moyen de les nettoyer. Si une erreur est retournée, chaque paramètre de sortie ou de sortie d’entrée doit être laissé à la valeur initialisée par l’appelant ou défini sur une valeur qui peut être nettoyée sans aucune action de la part de l’appelant. Par exemple, un paramètre de pointeur de `void ** ppv` sortie doit être laissé tel qu’il était en entrée ou peut être défini sur NULL ( `*ppv = NULL`).
  