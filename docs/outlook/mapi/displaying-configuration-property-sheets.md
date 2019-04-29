---
title: Affichage des feuilles de propriétés de configuration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421311"
---
# <a name="displaying-configuration-property-sheets"></a>Affichage des feuilles de propriétés de configuration

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de transport utilisent la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) pour implémenter des feuilles de propriétés de configuration. Lors de l'appel de **DoConfigPropSheet**, le fournisseur de transport transmet un pointeur vers un tableau de propriétés, ainsi que des informations sur la façon de les afficher. MAPI présente ensuite les propriétés à l'utilisateur au moyen d'une boîte de dialogue standard. Il est vivement recommandé d'utiliser ce mécanisme de feuille de propriétés lors de l'implémentation de votre fournisseur de transport en raison de l'avantage pour l'utilisateur d'une interface cohérente.
  
## <a name="transport-providers"></a>Fournisseurs de transport

Les fournisseurs de transport peuvent utiliser la fonction [BuildDisplayTable](builddisplaytable.md) pour simplifier la création d'une table d'affichage à utiliser avec **DoConfigPropSheet**. Les fournisseurs de transport peuvent également utiliser l'API de feuille de propriétés directement. Pour modifier les modifications apportées à la mémoire tampon des propriétés, les fournisseurs de transport peuvent utiliser la fonction [CreateIProp](createiprop.md) . Cela simplifie la gestion des annulations par l'utilisateur pendant que l'utilisateur modifie les valeurs stockées dans les propriétés. Si nécessaire, un fournisseur de transport peut également fournir une boîte de dialogue d'Assistant pour simplifier les tâches de configuration de l'utilisateur. 
  

