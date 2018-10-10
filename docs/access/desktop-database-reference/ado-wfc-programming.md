---
title: Programmation ADO/WFC
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88343d14a9419cbc3425e0c21dee08d243f2e697
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469598"
---
# <a name="adowfc-programming"></a>Programmation ADO/WFC


**S’applique à**: Access 2013 | Office 2013

ADO a été étendu pour Microsoft Visual J++ 6.0 afin de fonctionner avec Windows Foundation Classes (WFC) de la façon suivante. Un ensemble de classes Java a été implémenté pour étendre les interfaces ADO et créer des notifications destinées au programmeur Java ; les classes Java exposent également des fonctions qui retournent les types Java à l'utilisateur. Pour améliorer les performances, la classe Java accède directement aux types de données natifs dans l'objet rowset OLE DB et les retourne au programmeur Java en tant que types Java sans les avoir au préalable convertis en type variant. ADO a également été étendu de manière à utiliser des notifications d'événements dans l'infrastructure WFC.

ADO pour Windows Foundation Classes (ADO/WFC) prend en charge toutes les méthodes et propriétés ainsi que tous les objets et événements ADO standard. En revanche, les opérations qui requièrent un variant en tant que paramètre et sont très performantes dans Microsoft Visual Basic, sont moins performantes dans un langage tel que Visual J++. Pour cette raison, ADO/WFC comporte également des fonctions d'accesseur sur l'objet [Field](field-object-ado.md) qui prennent les types de données Java natifs plutôt que les types de données variant.

Pour des informations plus détaillées dans la documentation ADO sur les packages ADO/WFC, consultez [Index de la syntaxe ADO/WFC](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).

## <a name="referencing-the-library"></a>Référence de la bibliothèque

Pour importer les classes de données ADO/WFC dans votre projet, ajoutez la ligne suivante dans le code :

```java 
 
import com.ms.wfc.data.*; 
```

