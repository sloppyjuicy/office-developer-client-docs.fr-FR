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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308665"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="2fda8-102">Définition du format de marshaling du flux</span><span class="sxs-lookup"><span data-stu-id="2fda8-102">Setting DCOM stream marshaling format</span></span>


<span data-ttu-id="2fda8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fda8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fda8-p101">Un ordinateur client utilisant les composants de RDS 1.5 ou antérieur n'est pas compatible avec un serveur utilisant les composants de RDS 2.0 ou ultérieur. Lorsque DCOM est utilisé comme protocole sous-jacent, la prise en charge de RDS 2.0 ou ultérieur est plus efficace pour assurer le transport d'objets [Recordset](recordset-object-ado.md). Si votre client exécute des composants de RDS 1.5 ou antérieur, vous pouvez configurer votre serveur de façon à ce qu'il prenne en charge la version précédente de RDS (RDS 1.0) ou la version plus récente (RDS 2.0 ou ultérieur). Définissez une des entrées suivantes dans le Registre :</span><span class="sxs-lookup"><span data-stu-id="2fda8-p101">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later. When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects. If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later). Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="2fda8-108">\-or-</span><span class="sxs-lookup"><span data-stu-id="2fda8-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

