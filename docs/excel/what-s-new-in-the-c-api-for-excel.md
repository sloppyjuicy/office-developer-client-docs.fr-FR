---
title: Quelles sont les nouveautés de l’API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api c [excel 2007], quelles sont les nouveautés
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19782194"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Quelles sont les nouveautés de l’API C pour Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Conjointement avec Microsoft Excel 2013, le Kit de développement de logiciel (SDK) de Microsoft Excel 2013 XLL prend en charge les fonctionnalités suivantes.
  
- **Nouvelles fonctions**
    
    Le SDK XLL Microsoft Excel 2013 prend en charge les rappels à toutes les nouvelles fonctions de feuille de calcul dans Excel 2013. Pour plus d’informations sur l’appel de fonctions Excel 2013, voir [appel dans Excel à partir de la DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Fonctions asynchrones définies par l’utilisateur**
    
    Excel 2013 prend en charge l’appel de fonctions définies par l’utilisateur (UDF) en mode asynchrone, qui peut améliorer les performances en activant plusieurs calculs à exécuter en même temps. Pour plus d’informations sur les UDF asynchrones, voir [Fonctions Asynchronous User-Defined](asynchronous-user-defined-functions.md).
    
- **Connecteurs de cluster**
    
    Connecteurs de cluster activer les UDF à exécuter sur les clusters de calcul hautes performances. Pour plus d’informations sur la création de connecteurs de cluster, voir [Développement de connecteurs de Cluster Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Compléments XLL que vous souhaitez exécuter sur les clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster. Pour plus d’informations sur les fonctions que vous pouvez utiliser, voir [Référence des fonctions API Excel XLL SDK](excel-xll-sdk-api-function-reference.md) et des [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md). 
  
- **prise en charge 64 bits**
    
    Vous pouvez maintenant compiler et lier XLL 32 bits et 64 bits. Pour plus d’informations, voir [Création de XLL](creating-xlls.md).
    
## <a name="see-also"></a>Voir aussi



[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Programmation avec l�API�C dans Excel](programming-with-the-c-api-in-excel.md)
  
[Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)


[Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

