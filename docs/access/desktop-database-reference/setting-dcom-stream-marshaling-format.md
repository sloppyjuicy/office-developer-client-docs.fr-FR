---
title: Définition du format pour le marshaling de flux DCOM
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0c05a378624f118f1bf6f070273b686a2e50a6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470877"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="a300b-102">Définition du format pour le marshaling de flux DCOM</span><span class="sxs-lookup"><span data-stu-id="a300b-102">Setting DCOM Stream Marshaling Format</span></span>


<span data-ttu-id="a300b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a300b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a300b-p101">Un ordinateur client utilisant les composants de RDS 1.5 ou antérieur n'est pas compatible avec un serveur utilisant les composants de RDS 2.0 ou ultérieur. Lorsque DCOM est utilisé comme protocole sous-jacent, la prise en charge de RDS 2.0 ou ultérieur est plus efficace pour assurer le transport d'objets [Recordset](recordset-object-ado.md). Si votre client exécute des composants de RDS 1.5 ou antérieur, vous pouvez configurer votre serveur de façon à ce qu'il prenne en charge la version précédente de RDS (RDS 1.0) ou la version plus récente (RDS 2.0 ou ultérieur). Définissez une des entrées suivantes dans le Registre :</span><span class="sxs-lookup"><span data-stu-id="a300b-p101">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later. When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects. If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later). Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="a300b-108">\-ou -</span><span class="sxs-lookup"><span data-stu-id="a300b-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

