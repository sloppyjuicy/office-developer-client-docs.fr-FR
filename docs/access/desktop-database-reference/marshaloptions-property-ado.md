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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289769"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="3dd3d-102">MarshalOptions, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3dd3d-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="3dd3d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3dd3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3dd3d-104">Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="3dd3d-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3dd3d-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="3dd3d-105">Settings And Return Values</span></span>

<span data-ttu-id="3dd3d-p101">Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="3dd3d-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd3d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dd3d-108">Remarks</span></span>

<span data-ttu-id="3dd3d-109">Lors de l'utilisation d'un [objet Recordset](recordset-object-ado.md)côté client, les enregistrements qui ont été modifiés sur le client sont réécrits sur le niveau intermédiaire ou le serveur Web via une technique appelée marshaling, le processus d'empaquetage et l'envoi de paramètres de méthode d'interface à travers le thread ou limites de processus.</span><span class="sxs-lookup"><span data-stu-id="3dd3d-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="3dd3d-110">La définition de la propriété **MarshalOptions** peut améliorer les performances lorsque les données à distance modifiées sont marshalées pour être mises à jour vers le niveau intermédiaire ou le serveur Web.</span><span class="sxs-lookup"><span data-stu-id="3dd3d-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="3dd3d-111">**Utilisation des services de données à distance** Cette propriété est utilisée uniquement sur un **objet Recordset**côté client.</span><span class="sxs-lookup"><span data-stu-id="3dd3d-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

