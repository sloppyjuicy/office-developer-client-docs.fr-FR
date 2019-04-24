---
title: Nouveautés de l'API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- API c [Excel 2007], nouveautés
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310268"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Nouveautés de l'API C pour Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Conjointement avec Microsoft Excel 2013, le kit de développement logiciel (SDK) XLL Microsoft Excel 2013 inclut la prise en charge des fonctionnalités suivantes.
  
- **Nouvelles fonctions**
    
    Le kit de développement XLL Microsoft Excel 2013 prend en charge le rappel de toutes les nouvelles fonctions de feuille de calcul dans Excel 2013. Pour plus d'informations sur l'appel de fonctions Excel 2013, consultez [la rubrique appel dans Excel à partir de la dll ou XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Fonctions asynchrones définies par l'utilisateur**
    
    Excel 2013 prend en charge l'appel de fonctions définies par l'utilisateur (UDF) de manière asynchrone, ce qui peut améliorer les performances en permettant l'exécution de plusieurs calculs en même temps. Pour plus d'informations sur les fonctions définies par l'utilisateur asynchrones, voir [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).
    
- **Connecteurs de cluster**
    
    Les connecteurs de cluster permettent aux UDF de s'exécuter sur des clusters de calcul à hautes performances. Pour plus d'informations sur la création de connecteurs de cluster, voir [développement de connecteurs de cluster Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Les compléments XLL que vous envisagez d'exécuter sur des clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster. Pour plus d'informations sur les fonctions que vous pouvez utiliser, reportez-vous à la rubrique [Excel XLL SDK API Reference](excel-xll-sdk-api-function-reference.md) and [cluster safe](cluster-safe-functions.md)functions. 
  
- **Prise en charge de 64 bits**
    
    Vous pouvez maintenant compiler et lier les XLL 32 bits et 64 bits. Pour plus d'informations, consultez la rubrique [creatIng XLL](creating-xlls.md).
    
## <a name="see-also"></a>Voir aussi



[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Programmation avec l�API�C dans Excel](programming-with-the-c-api-in-excel.md)
  
[Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)


[Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

