---
title: Didacticiel RDS (Visual J ++)
TOCTitle: RDS tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e23af46ac7aab267eb5788aa4790d5c568f23609
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946124"
---
# <a name="rds-tutorial-visual-j"></a>Didacticiel RDS (Visual J ++)


**S’applique à**: Access 2013, Office 2013

ADO/WFC ne suit pas intégralement le modèle d'objet RDS en cela qu'il n'implémente pas l'objet [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC implémente uniquement la classe côté client[RDS.DataSpace](dataspace-object-rds.md).

La classe **DataSpace** implémente une seule méthode, [CreateObject](createobject-method-rds.md), qui retourne un objet [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)). La classe **DataSpace** implémente également la propriété [InternetTimeout](internettimeout-property-rds.md).

La classe **ObjectProxy** implémente une seule méthode, call, qui peut appeler n'importe quel objet métier côté serveur.

**Point de départ du didacticiel.**

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

**Fin du didacticiel.**

