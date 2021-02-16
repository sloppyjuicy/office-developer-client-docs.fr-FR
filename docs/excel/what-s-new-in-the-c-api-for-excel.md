---
title: Nouveautés de l’API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], nouveautés
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439687"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Nouveautés de l’API C pour Excel

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Conjointement avec Microsoft Excel 2013, le Kit de développement logiciel (SDK) XLL Microsoft Excel 2013 inclut la prise en charge des fonctionnalités suivantes.
  
- **Nouvelles fonctions**
    
    Le SDK XLL Microsoft Excel 2013 prend en charge les appels vers toutes les nouvelles fonctions de feuille de calcul dans Excel 2013. Pour plus d’informations sur l’appel de fonctions Excel 2013, voir Appel dans Excel à partir de [la DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Fonctions asynchrones définies par l’utilisateur**
    
    Excel 2013 prend en charge l’appel asynchrone des fonctions définies par l’utilisateur (UDF), ce qui peut améliorer les performances en permettant à plusieurs calculs de s’exécuter en même temps. Pour plus d’informations sur les fonctions UDF [asynchrones, voir Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).
    
- **Connecteurs de cluster**
    
    Les connecteurs de cluster permettent aux UDF de s’exécuter sur des clusters de calcul hautes performances. Pour plus d’informations sur la création de connecteurs de cluster, voir [Développement de connecteurs de cluster Excel.](developing-excel-cluster-connectors.md)
    
    > [!NOTE]
    > Les add-ins XLL que vous avez l’intention d’exécuter sur des clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster. Pour plus d’informations sur les fonctions que vous pouvez utiliser, voir Référence des fonctions api [du SDK XLL Excel](excel-xll-sdk-api-function-reference.md) et [Fonctions sécurisées du cluster.](cluster-safe-functions.md) 
  
- **Prise en charge 64 bits**
    
    Vous pouvez désormais compiler et lier des XL 32 bits et 64 bits. Pour plus d’informations, voir [Création de XLS.](creating-xlls.md)
    
## <a name="see-also"></a>Voir aussi



[Développement de XLL de Excel](developing-excel-xlls.md)
  
[Programmation avec l�API C dans Excel](programming-with-the-c-api-in-excel.md)
  
[Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)


[Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

