---
title: Allocation et libération de la mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dc97abcb4b316b696032f2788f4e653717e1396b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782910"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Allocation et libération de la mémoire dans MAPI

  
  
**S’applique à**: Outlook 
  
Outre la spécification de l’affectation et libérer de la mémoire, MAPI définit un modèle pour savoir quand la mémoire transmise entre la méthode d’interface publique et la fonction API appels doivent être libérés. Le modèle s’applique uniquement à la mémoire allouée pour les paramètres qui ne sont pas des pointeurs vers des interfaces, telles que des chaînes et des pointeurs vers des structures. Pointeurs d’interface utilisent le décompte de références mécanisme implémentés par le biais de **IUnknown**. Lors de l’allocation et la libération non MAPI liées mémoire en interne au sein d’une application cliente ou d’un fournisseur de services, utilisez le mécanisme significatif. 
  
Le modèle définit les paramètres d’un des trois types. Ils peuvent être saisis paramètres, définis par l’appelant avec des informations pour être utilisé par la fonction ou la méthode, paramètres de sortie, défini par la méthode ou la fonction appelée et renvoyé à l’appelant, ou une combinaison des deux types de paramètres d’entrée / sortie. Paramètres de sortie sont souvent des pointeurs vers des données ou des pointeurs vers des pointeurs vers des données. Bien que la fonction appelée est chargée d’allouer les données pour les paramètres de sortie, l’appelant alloue de la mémoire pour le pointeur. 
  
Les règles d’allouer et de libérer de la mémoire pour ces types de paramètres sont expliquées dans le tableau suivant.
  
|**Type**|**Allocation de mémoire**|**Version de la mémoire**|
|:-----|:-----|:-----|
|Input  <br/> |L’appelant est chargé et permettre utiliser n’importe quel mécanisme.  <br/> |L’appelant est chargé et permettre utiliser n’importe quel mécanisme.  <br/> |
|Output  <br/> |Fonction appelée est chargée et doit utiliser **MAPIAllocateBuffer**. Pour plus d’informations, voir [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |L’appelant est chargé et doit utiliser **MAPIFreeBuffer**. Pour plus d’informations, voir [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Entrées / sorties  <br/> |L’appelant est responsable de l’allocation initiale et la fonction appelée peuvent réaffecter si nécessaire à l’aide de **MAPIAllocateBuffer**.  <br/> |Fonction appelée est chargée de libérer initiale si réallocation est requise. L’appelant doit libérer la valeur de retour finale.  <br/> |
   
Au cours des conditions d’échec, l’implémentation des méthodes d’interface doit attention aux paramètres de sortie et d’entrée / sortie car l’appelant a généralement aucun moyen pour les nettoyer. Si une erreur est renvoyée, puis chaque sortie ou le paramètre d’entrée / sortie doit soit rester à la valeur initialisée par l’appelant ou une valeur qui peut être nettoyés sans aucune action de la part de l’appelant. Par exemple, un pointeur-paramètre de sortie de `void ** ppv` doit rester tel qu’il a été entrée ou peut être définie sur NULL ( `*ppv = NULL`).
  

