---
title: LockTypeEnum, énumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: e1258e312648d36c99671dc1013520e36316dec3
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627423"
---
# <a name="locktypeenum-enumeration-dao"></a>LockTypeEnum, énumeration (DAO)


**S’applique à** : Access 2013, Office 2013

Spécifie le type de verrouillage des enregistrements utilisé lors de l'ouverture d'un jeu d'enregistrements.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>Accès concurrentiel optimiste basé sur l'ID d'enregistrement. Le curseur compare l'ID d'enregistrement de l'ancien et du nouvel enregistrement pour déterminer si des modifications ont été apportées depuis le dernier accès à l'enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Permet des mises à jour par lot optimistes (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Accès concurrentiel optimiste basé sur les valeurs d'enregistrement. Le curseur compare les valeurs des données dans l'ancien et le nouvel enregistrement pour déterminer si des modifications ont été apportées depuis le dernier accès à l'enregistrement (espaces de travail ODBCDirect uniquement).</p>

> [!NOTE]
> Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Accès concurrentiel pessimiste. Le curseur utilise le niveau de verrouillage le plus bas qui permet de garantir la mise à jour de l'enregistrement.</p></td>
</tr>
</tbody>
</table>

