---
title: Programmation ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63cfbdf2219179536bd4726d16e49fd05a84f4a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607548"
---
# <a name="adowfc-programming"></a>Programmation ADO/WFC

**S’applique à** : Access 2013, Office 2013

ADO a été étendu pour Microsoft Visual J++ 6.0 afin de fonctionner avec Windows Foundation Classes (WFC) de la façon suivante. Un ensemble de classes Java a été implémenté pour étendre les interfaces ADO et créer des notifications destinées au programmeur Java ; les classes Java exposent également des fonctions qui retournent les types Java à l'utilisateur. Pour améliorer les performances, la classe Java accède directement aux types de données natifs dans l'objet rowset OLE DB et les retourne au programmeur Java en tant que types Java sans les avoir au préalable convertis en type variant. ADO a également été étendu de manière à utiliser des notifications d'événements dans l'infrastructure WFC.

ADO pour Windows Foundation Classes (ADO/WFC) prend en charge toutes les méthodes et propriétés ainsi que tous les objets et événements ADO standard. En revanche, les opérations qui requièrent un variant en tant que paramètre et sont très performantes dans Microsoft Visual Basic, sont moins performantes dans un langage tel que Visual J++. Pour cette raison, ADO/WFC comporte également des fonctions d'accesseur sur l'objet [Field](field-object-ado.md) qui prennent les types de données Java natifs plutôt que les types de données variant.

Pour des informations plus détaillées dans la documentation ADO sur les packages ADO/WFC, consultez [Index de la syntaxe ADO/WFC](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).

## <a name="referencing-the-library"></a>Référencement de la bibliothèque

Pour importer les classes de données ADO/WFC dans votre projet, ajoutez la ligne suivante dans le code :

```java 
 
import com.ms.wfc.data.*; 
```

