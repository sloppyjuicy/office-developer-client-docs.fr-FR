---
title: Définition du format de marshaling du flux
TOCTitle: Setting DCOM stream marshaling format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09463552faff9c4b74b73379385ab8ba55b4f62c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698042"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Définition du format de marshaling du flux


**S’applique à**: Access 2013, Office 2013

Un ordinateur client utilisant les composants de RDS 1.5 ou antérieur n'est pas compatible avec un serveur utilisant les composants de RDS 2.0 ou ultérieur. Lorsque DCOM est utilisé comme protocole sous-jacent, la prise en charge de RDS 2.0 ou ultérieur est plus efficace pour assurer le transport d'objets [Recordset](recordset-object-ado.md). Si votre client exécute des composants de RDS 1.5 ou antérieur, vous pouvez configurer votre serveur de façon à ce qu'il prenne en charge la version précédente de RDS (RDS 1.0) ou la version plus récente (RDS 2.0 ou ultérieur). Définissez une des entrées suivantes dans le Registre :

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-ou -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

