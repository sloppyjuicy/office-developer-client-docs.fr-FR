---
title: Initialisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420947"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisation des utilitaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si la seule partie de MAPI que vous devez utiliser est les utilitaires : les interfaces et les fonctions déclarées dans MAPIUTIL. Fichier d’en-tête H tel que **IPropData** et **ITableData** : vous n’avez pas besoin d’appeler **MAPIInitialize** pour l’initialisation. Pour plus d’informations, voir [IPropData : IMAPIProp,](ipropdataimapiprop.md) [ITableData : IUnknown](itabledataiunknown.md)et [MAPIInitialize](mapiinitialize.md). Appelez plutôt la **fonction ScInitMapiUtil.** Pour plus d’informations, [voir ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permet aux applications clientes d’utiliser des fonctions utilitaires et des méthodes qui nécessitent des allocations MAPI, mais qui ne les demandent pas explicitement. 
  
Au moment de l’arrêt, appelez **DeinitMapiUtil** pour libérer des ressources connectées aux utilitaires. N’appelez **pas MAPIUninitialize**. Pour plus d’informations, [voir DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).
  
N’ignorez pas que l’interface **ITableData** ne prend pas en charge les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** plutôt que **MAPIInitialize**. 
  

