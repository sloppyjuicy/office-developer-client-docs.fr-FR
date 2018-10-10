---
title: NativeError, propriété (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472476"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="4e8df-102">NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4e8df-102">NativeError Property (ADO)</span></span>


<span data-ttu-id="4e8df-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e8df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4e8df-104">Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.</span><span class="sxs-lookup"><span data-stu-id="4e8df-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e8df-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4e8df-105">Return Value</span></span>

<span data-ttu-id="4e8df-106">Renvoie une valeur de type **Long** qui indique le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="4e8df-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e8df-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e8df-107">Remarks</span></span>

<span data-ttu-id="4e8df-p101">Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.</span><span class="sxs-lookup"><span data-stu-id="4e8df-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

