---
title: Initialisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784310"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisation des utilitaires MAPI

  
  
**S’applique à**: Outlook 
  
Si la seule partie de MAPI que vous devrez utiliser sont les utilitaires, les interfaces et les fonctions déclarées dans MAPIUTIL de MAPI. Fichier d’en-tête H telles que **IPropData** et **ITableData** — vous n’avez pas besoin d’appeler **exécuter MAPIInitialize** pour l’initialisation. Pour plus d’informations, voir [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)et [exécuter MAPIInitialize](mapiinitialize.md). Au lieu de cela, appelez la fonction **ScInitMapiUtil** . Pour plus d’informations, voir [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permet aux applications de client à utiliser les fonctions utilitaires et des méthodes qui requièrent des allocateurs MAPI, mais qui ne demandent pas les explicitement. 
  
Au moment de l’arrêt, passer un appel à **DeinitMapiUtil** pour libérer des ressources liées aux utilitaires. N’appelez pas **MAPIUninitialize**. Pour plus d’informations, voir [DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).
  
Sachez que l’interface **ITableData** ne gère pas les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** plutôt que **d’exécuter MAPIInitialize**. 
  

