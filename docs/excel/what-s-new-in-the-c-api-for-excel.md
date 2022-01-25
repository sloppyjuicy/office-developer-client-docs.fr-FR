---
title: Nouveautés de l’API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], nouveautés
ms.localizationpriority: medium
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
ms.openlocfilehash: 4a63beb8a3021faa0385d6399964a902b62b0630
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199283"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Nouveautés de l’API C pour Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Conjointement avec Microsoft Excel 2013, Microsoft Excel 2013 Kit de développement logiciel (SDK) XLL inclut la prise en charge des fonctionnalités suivantes.
  
- **Nouvelles fonctions**
    
    Le Microsoft Excel 2013 SDK XLL prend en charge les appels vers toutes les nouvelles fonctions de feuille de calcul Excel 2013. Pour plus d’informations sur Excel fonctions 2013, consultez la Excel à partir de la DLL ou [XLL.](calling-into-excel-from-the-dll-or-xll.md)
    
- **Fonctions asynchrones définies par l’utilisateur**
    
    Excel 2013 prend en charge l’appel asynchrone des fonctions définies par l’utilisateur (UDF), ce qui peut améliorer les performances en permettant à plusieurs calculs de s’exécuter en même temps. Pour plus d’informations sur les fonctions UDF [asynchrones, voir Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).
    
- **Connecteurs de cluster**
    
    Les connecteurs de cluster permettent aux UDF de s’exécuter sur des clusters de calcul hautes performances. Pour plus d’informations sur la création de connecteurs de cluster, [voir Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Les add-ins XLL que vous avez l’intention d’exécuter sur des clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster. Pour plus d’informations sur les fonctions que vous pouvez utiliser, voir Excel référence des fonctions de [l’API du SDK XLL](excel-xll-sdk-api-function-reference.md) et les fonctions Coffre [cluster.](cluster-safe-functions.md) 
  
- **Prise en charge 64 bits**
    
    Vous pouvez désormais compiler et lier des XL 32 bits et 64 bits. Pour plus d’informations, voir [Création de XLS.](creating-xlls.md)
    
## <a name="see-also"></a>Voir aussi



[Développement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Programmation avec l�API C dans Excel](programming-with-the-c-api-in-excel.md)
  
[Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)


[Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

