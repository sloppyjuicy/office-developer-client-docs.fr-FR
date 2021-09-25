---
title: Allocation et libération de mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5a0d6dd27d36c6631e5a66e522fb1f0fe6223e11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567864"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Allocation et libération de mémoire dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
En plus de spécifier comment allouer et libérer de la mémoire, MAPI définit un modèle pour savoir quand la mémoire transmise entre la méthode d’interface publique et les appels de fonction API doit être libérée. Le modèle s’applique uniquement à la mémoire allouée pour les paramètres qui ne sont pas des pointeurs vers des interfaces, tels que des chaînes et des pointeurs vers des structures. Les pointeurs d’interface utilisent le mécanisme de comptage de référence implémenté via **IUnknown**. Lorsque vous allouez et libérez de la mémoire non liée à MAPI en interne au sein d’une application cliente ou d’un fournisseur de services, utilisez n’importe quel mécanisme logique. 
  
Le modèle définit les paramètres comme l’un des trois types. Il peut s’agit de paramètres d’entrée, définies par l’appelant avec des informations à utiliser par la fonction ou la méthode appelée, des paramètres de sortie, définies par la fonction ou méthode appelée et renvoyées à l’appelant, ou des paramètres d’entrée/sortie, une combinaison des deux types. Les paramètres de sortie sont souvent des pointeurs vers des données ou des pointeurs vers des données. Bien que la fonction appelée soit responsable de l’allocation des données pour les paramètres de sortie, l’appelant alloue la mémoire pour le pointeur. 
  
Les règles d’allocation et de libération de mémoire pour ces types de paramètres sont expliquées dans le tableau suivant.
  
|**Type (Type)**|**Allocation de mémoire**|**Libération de mémoire**|
|:-----|:-----|:-----|
|Input  <br/> |L’appelant est responsable et peut utiliser n’importe quel mécanisme.  <br/> |L’appelant est responsable et peut utiliser n’importe quel mécanisme.  <br/> |
|Sortie  <br/> |La fonction appelée est responsable et doit utiliser **MAPIAllocateBuffer**. Pour plus d’informations, [voir MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |L’appelant est responsable et doit utiliser **MAPIFreeBuffer**. Pour plus d’informations, [voir MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Input-output  <br/> |L’appelant est responsable de l’allocation initiale et la fonction appelée peut réaffecter si nécessaire à l’aide de **MAPIAllocateBuffer**.  <br/> |La fonction appelée est responsable de la libération initiale si la réaffectation est nécessaire. L’appelant doit libérer la valeur de retour finale.  <br/> |
   
Dans les conditions d’échec, les implémenteurs de méthodes d’interface doivent être attentifs aux paramètres de sortie et de sortie d’entrée, car l’appelant n’a généralement aucun moyen de les nettoyer. Si une erreur est renvoyée, chaque paramètre de sortie ou de sortie d’entrée doit être laissé à la valeur initialisée par l’appelant ou être paramétrez sur une valeur qui peut être nettoyée sans aucune action de la part de l’appelant. Par exemple, un paramètre de pointeur de sortie doit être laissé tel qu’il était en entrée ou peut  `void ** ppv` être définie sur NULL (  `*ppv = NULL` ).
  

