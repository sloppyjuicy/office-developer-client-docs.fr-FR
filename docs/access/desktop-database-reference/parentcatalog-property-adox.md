---
title: ParentCatalog, propriété (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707457"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="04b1d-102">ParentCatalog, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="04b1d-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="04b1d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04b1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04b1d-104">Spécifie le catalogue parent d'une table ou colonne afin de fournir l'accès à des propriétés spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="04b1d-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="04b1d-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="04b1d-105">Settings and return values</span></span>

<span data-ttu-id="04b1d-p101">Définit et renvoie un objet [Catalog](catalog-object-adox.md). En affectant à **ParentCatalog** un objet **Catalog** ouvert, vous pouvez accéder aux propriétés spécifiques à un fournisseur avant d'ajouter une table ou une colonne à une collection **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="04b1d-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b1d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="04b1d-108">Remarks</span></span>

<span data-ttu-id="04b1d-p102">Certains fournisseurs de données permettent uniquement d'écrire des valeurs de propriétés qui leur sont spécifiques lors de la création (lorsque vous ajoutez une table ou une colonne à sa collection **Catalog** ). Pour accéder à ces propriétés avant d'ajouter ces objets à un objet **Catalog**, spécifiez d'abord l'objet **Catalog** dans la propriété **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="04b1d-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="04b1d-111">Une erreur se produit lorsque la table ou la colonne est ajoutée à un objet **Catalog** différent de celui spécifié dans la propriété **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="04b1d-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>

