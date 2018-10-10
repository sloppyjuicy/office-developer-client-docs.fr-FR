---
title: SQLState, propriété (ADO)
TOCTitle: SQLState Property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aead95e4276d61d69ae6ba5a86974cbe630f9043
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470745"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="62999-102">SQLState, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="62999-102">SQLState Property (ADO)</span></span>


<span data-ttu-id="62999-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62999-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62999-104">Indique l'état SQL d'un objet [Error](error-object-ado.md) donné.</span><span class="sxs-lookup"><span data-stu-id="62999-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="62999-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62999-105">Return Value</span></span>

<span data-ttu-id="62999-106">Renvoie une valeur **String** de 5 caractères qui, conformément à la norme ANSI SQL, indique le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="62999-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62999-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="62999-107">Remarks</span></span>

<span data-ttu-id="62999-p101">Utilisez la propriété **SQLState** pour lire le code d'erreur à 5 caractères renvoyé par le fournisseur lorsqu'une erreur se produit lors du traitement d'une instruction SQL. Par exemple, lorsque l'on utilise le fournisseur Microsoft OLE DB pour ODBC avec une base de données Microsoft SQL Server, les codes d'erreur d'état SQL sont issus d'ODBC ; ils reposent soit sur des erreurs spécifiques à ODBC, soit sur des erreurs provenant de Microsoft SQL Server, et sont ensuite mappés sur des erreurs ODBC. Ces codes d'erreur sont documentés dans la norme ANSI SQL, mais peuvent être implémentés différemment dans d'autres sources de données.</span><span class="sxs-lookup"><span data-stu-id="62999-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

