---
title: Initialisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7fe01c60193dda5cd9faa1e8723246475f5dd66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571632"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisation des utilitaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si la seule partie de MAPI que vous devez utiliser est les utilitaires : les interfaces et les fonctions déclarées dans MAPIUTIL. Fichier d’en-tête H tel que **IPropData** et **ITableData** : vous n’avez pas besoin d’appeler **MAPIInitialize** pour l’initialisation. Pour plus d’informations, voir [IPropData : IMAPIProp,](ipropdataimapiprop.md) [ITableData : IUnknown](itabledataiunknown.md)et [MAPIInitialize](mapiinitialize.md). Appelez plutôt la **fonction ScInitMapiUtil.** Pour plus d’informations, [voir ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permet aux applications clientes d’utiliser des fonctions utilitaires et des méthodes qui nécessitent des allocations MAPI, mais qui ne les demandent pas explicitement. 
  
Au moment de l’arrêt, appelez **DeinitMapiUtil** pour libérer des ressources connectées aux utilitaires. N’appelez **pas MAPIUninitialize**. Pour plus d’informations, [voir DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).
  
N’ignorez pas que l’interface **ITableData** ne prend pas en charge les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** plutôt que **MAPIInitialize**. 
  

