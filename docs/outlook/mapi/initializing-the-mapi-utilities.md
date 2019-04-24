---
title: Initialisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317219"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisation des utilitaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si la seule partie de MAPI que vous devez utiliser est les utilitaires, les interfaces et les fonctions déclarées dans la MAPIUTIL de MAPI. H, par exemple **IPropData** et **ITableData** , il n'est pas nécessaire d'appeler **MAPIInitialize** pour l'initialisation. Pour plus d'informations, voir [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)et [MAPIInitialize](mapiinitialize.md). À la place, appelez la fonction **ScInitMapiUtil** . Pour plus d'informations, consultez la rubrique [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permet aux applications clientes d'utiliser des fonctions et des méthodes utilitaires qui nécessitent des allocateurs MAPI, mais qui ne les demandent pas explicitement. 
  
Au moment de l'arrêt, effectuez un appel à **DeinitMapiUtil** pour libérer les ressources connectées aux utilitaires. N'appelez pas **MAPIUninitialize**. Pour plus d'informations, voir [DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).
  
N'oubliez pas que l'interface **ITableData** ne prend pas en charge les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** et non **MAPIInitialize**. 
  

