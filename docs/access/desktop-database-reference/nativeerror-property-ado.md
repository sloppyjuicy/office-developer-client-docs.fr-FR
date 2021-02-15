---
title: NativeError, propriété (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288609"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="d1b75-102">NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d1b75-102">NativeError property (ADO)</span></span>


<span data-ttu-id="d1b75-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1b75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1b75-104">Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.</span><span class="sxs-lookup"><span data-stu-id="d1b75-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1b75-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1b75-105">Return value</span></span>

<span data-ttu-id="d1b75-106">Renvoie une valeur de type **Long** qui indique le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="d1b75-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b75-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1b75-107">Remarks</span></span>

<span data-ttu-id="d1b75-p101">Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.</span><span class="sxs-lookup"><span data-stu-id="d1b75-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

