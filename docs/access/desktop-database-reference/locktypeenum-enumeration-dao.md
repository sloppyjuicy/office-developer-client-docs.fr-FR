---
title: LockTypeEnum, énumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289856"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="1ac01-102">LockTypeEnum, énumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ac01-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="1ac01-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ac01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ac01-104">Spécifie le type de verrouillage des enregistrements utilisé lors de l'ouverture d'un jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="1ac01-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ac01-105">Nom</span><span class="sxs-lookup"><span data-stu-id="1ac01-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1ac01-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ac01-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1ac01-107">Description</span><span class="sxs-lookup"><span data-stu-id="1ac01-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ac01-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="1ac01-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="1ac01-109">3</span><span class="sxs-lookup"><span data-stu-id="1ac01-109">3.</span></span></p></td>
<td><p><span data-ttu-id="1ac01-p101">Accès concurrentiel optimiste basé sur l'ID d'enregistrement. Le curseur compare l'ID d'enregistrement de l'ancien et du nouvel enregistrement pour déterminer si des modifications ont été apportées depuis le dernier accès à l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1ac01-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac01-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="1ac01-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="1ac01-113">5</span><span class="sxs-lookup"><span data-stu-id="1ac01-113">5.</span></span></p></td>
<td><p><span data-ttu-id="1ac01-114">Permet des mises à jour par lot optimistes (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="1ac01-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac01-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="1ac01-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="1ac01-116">1</span><span class="sxs-lookup"><span data-stu-id="1ac01-116">-1</span></span></p></td>
<td><p><span data-ttu-id="1ac01-p102">Accès concurrentiel optimiste basé sur les valeurs d'enregistrement. Le curseur compare les valeurs des données dans l'ancien et le nouvel enregistrement pour déterminer si des modifications ont été apportées depuis le dernier accès à l'enregistrement (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="1ac01-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="1ac01-p103">Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1ac01-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac01-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="1ac01-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="1ac01-122">2</span><span class="sxs-lookup"><span data-stu-id="1ac01-122">2.</span></span></p></td>
<td><p><span data-ttu-id="1ac01-p104">Accès concurrentiel pessimiste. Le curseur utilise le niveau de verrouillage le plus bas qui permet de garantir la mise à jour de l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1ac01-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

