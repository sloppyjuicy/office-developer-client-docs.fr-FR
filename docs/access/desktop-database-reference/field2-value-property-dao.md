---
title: Field2. Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292628"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="df55a-102">Field2. Value, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="df55a-102">Field2.Value property (DAO)</span></span>


<span data-ttu-id="df55a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df55a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df55a-104">Définit ou renvoie la valeur d'un objet.</span><span class="sxs-lookup"><span data-stu-id="df55a-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="df55a-105">**Variant** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="df55a-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df55a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df55a-106">Syntax</span></span>

<span data-ttu-id="df55a-107">*expression* . Valeur</span><span class="sxs-lookup"><span data-stu-id="df55a-107">*expression* .Value</span></span>

<span data-ttu-id="df55a-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="df55a-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df55a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="df55a-109">Remarks</span></span>

<span data-ttu-id="df55a-110">Le paramètre ou la valeur de retour est un type de données Variant qui correspond à une valeur adaptée au type de données, tel qu'il est défini par la propriété **Type** d'un objet.</span><span class="sxs-lookup"><span data-stu-id="df55a-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="df55a-111">En règle générale, la propriété **Value** permet d'extraire et de modifier les données des objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="df55a-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="df55a-p102">La propriété **Value** est la propriété par défaut des objets **Field2**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en leur faisant directement référence plutôt qu'en définissant la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="df55a-p102">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="df55a-114">Une erreur capturable survient si vous tentez de définir ou de retourner la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field2** de la collection **Fields** d'un objet **TableDef**) entraîne une erreur capturable.</span><span class="sxs-lookup"><span data-stu-id="df55a-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <span data-ttu-id="df55a-115">Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles sont formattées à l'aide d'une notation scientifique dans un espace de travail Microsoft Access, mais apparaissent comme des valeurs décimales normales dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="df55a-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


