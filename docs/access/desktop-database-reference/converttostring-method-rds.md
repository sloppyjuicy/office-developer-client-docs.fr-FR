---
title: ConvertToString, méthode (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa1a4326cf318a9cbcddf8ebcdf584543ac8ebfb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471844"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="b97c4-102">ConvertToString, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="b97c4-102">ConvertToString Method (RDS)</span></span>


<span data-ttu-id="b97c4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b97c4-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="b97c4-104">Convertit un objet [Recordset](recordset-object-ado.md) en chaîne MIME qui représente les données du jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="b97c4-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b97c4-105">Syntax</span></span>

<span data-ttu-id="b97c4-106">*DataFactory*. ConvertToString (*jeu d’enregistrements*)</span><span class="sxs-lookup"><span data-stu-id="b97c4-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="b97c4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b97c4-107">Parameters</span></span>

  - <span data-ttu-id="b97c4-108">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="b97c4-108">*DataFactory*</span></span>

  - <span data-ttu-id="b97c4-109">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="b97c4-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="b97c4-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="b97c4-110">*Recordset*</span></span>

  - <span data-ttu-id="b97c4-111">Variable objet représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b97c4-111">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97c4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b97c4-112">Remarks</span></span>

<span data-ttu-id="b97c4-113">Avec des fichiers .asp, utilisez **ConvertToString** pour incorporer l'objet **Recordset** dans une page HTML générée sur le serveur afin de le transporter sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b97c4-113">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="b97c4-114">**ConvertToString** commence par charger l'objet **Recordset** dans les tables du service de curseur, puis génère un flux au format MIME.</span><span class="sxs-lookup"><span data-stu-id="b97c4-114">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="b97c4-p101">Sur le client, RDS (Remote Data Service) peut reconvertir la chaîne MIME en un objet **Recordset** parfaitement fonctionnel. Cette méthode fonctionne bien pour gérer moins de 400 lignes de données comportant moins de 1024 octets par ligne, mais il faut l'éviter si vous voulez diffuser en continu des données BLOB et des jeux de résultats volumineux via HTTP. En effet, la chaîne n'est pas compressée et le transport, via HTTP, d'ensembles importants de données prend un temps considérable comparé au format de transmission Tablegram optimisé, défini et déployé par RDS (Remote Data Service) en tant que format de protocole de transport natif.</span><span class="sxs-lookup"><span data-stu-id="b97c4-p101">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**. It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row. You shouldn't use it for streaming BLOB data and large result sets over HTTP. No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b97c4-p102">[!REMARQUE] Si vous utilisez des pages ASP pour incorporer la chaîne MIME résultante dans une page HTML cliente, sachez que les versions de VBScript antérieures à 2.0 limitent la taille de la chaîne à 32 Ko. Si cette limite est dépassée, une erreur est retournée. Par conséquent, essayez de limiter la portée de la requête lorsque vous procédez à une incorporation MIME via des fichiers .asp. Pour résoudre ce problème, téléchargez la dernière version de VBScript à partir du <A href="https://www.microsoft.com/downloads/en/default.aspx">Centre de téléchargement Microsoft</A>.</span><span class="sxs-lookup"><span data-stu-id="b97c4-p102">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K. If this limit is exceeded, an error is returned. Keep the query scope relatively small when using MIME embedding via .asp files. To fix this, download the latest version of VBScript from the <A href="https://www.microsoft.com/downloads/en/default.aspx">Microsoft Download Center</A>.</span></span></P>


