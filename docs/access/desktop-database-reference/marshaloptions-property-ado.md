---
title: MarshalOptions, propriété (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704594"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="e57b2-102">MarshalOptions, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e57b2-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="e57b2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e57b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e57b2-104">Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="e57b2-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e57b2-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="e57b2-105">Settings And Return Values</span></span>

<span data-ttu-id="e57b2-p101">Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="e57b2-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e57b2-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e57b2-108">Remarks</span></span>

<span data-ttu-id="e57b2-109">Lorsque vous utilisez un [jeu d’enregistrements](recordset-object-ado.md)du côté client, les enregistrements qui ont été modifiés sur le client sont réécrits au niveau intermédiaire ou au serveur web via une technique appelée marshaling, le processus d’empaquetage et d’envoi des paramètres de méthode d’interface entre les threads ou limites de processus.</span><span class="sxs-lookup"><span data-stu-id="e57b2-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="e57b2-110">Définition de la propriété **MarshalOptions** peut améliorer les performances lors du marshaling de données distantes modifiées pour mettre à jour au niveau intermédiaire ou au serveur web.</span><span class="sxs-lookup"><span data-stu-id="e57b2-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="e57b2-111">**L’utilisation du Service de données à distance** Cette propriété est utilisée uniquement sur un **jeu d’enregistrements**du côté client.</span><span class="sxs-lookup"><span data-stu-id="e57b2-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

