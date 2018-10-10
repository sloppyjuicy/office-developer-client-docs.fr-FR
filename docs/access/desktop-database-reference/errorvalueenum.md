---
title: ErrorValueEnum (référence de base de données du bureau Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de7f19c119c3161ece57344b911fcca36a1a8a3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470998"
---
# <a name="errorvalueenum"></a><span data-ttu-id="6ed34-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="6ed34-102">ErrorValueEnum</span></span>


<span data-ttu-id="6ed34-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ed34-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ed34-104">Spécifie le type d'erreur d'exécution ADO.</span><span class="sxs-lookup"><span data-stu-id="6ed34-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="6ed34-105">Trois formes d'erreur sont répertoriées :</span><span class="sxs-lookup"><span data-stu-id="6ed34-105">Three forms of the error number are listed:</span></span>

  - <span data-ttu-id="6ed34-p101">Décimale positive  Les deux octets faibles du nombre complet au format décimal. Ce nombre est affiché dans la boîte de dialogue par défaut des messages d'erreur de Visual Basic. Exemple : Erreur d'exécution '3707''.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

  - <span data-ttu-id="6ed34-109">Décimale négative  La conversion décimale du numéro d'erreur complet.</span><span class="sxs-lookup"><span data-stu-id="6ed34-109">Negative decimal — The decimal translation of the full error number.</span></span>

  - <span data-ttu-id="6ed34-p102">Hexadécimale — La représentation héxadécimale du numéro d'erreur complet. Le code de fonction Windows est dans le quatrième chiffre. Le code de fonction des numéros d'erreurs ADO est *A*. Exemple : 0x800***A***0E7B.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p102">Hexadecimal — The hexadecimal representation of the full error number. The Windows facility code is in the fourth digit. The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6ed34-p103">Les erreurs OLE DB peuvent être transmises à votre application ADO. En général, elles peuvent être identifiées par un code de fonction Windows <EM>4</EM>. Exemple : 0x800<STRONG><EM>4</EM></STRONG>.... Pour plus d'informations sur ces numéros, consultez le chapitre 16 du manuel <EM>OLE DB Programmer's Reference.</EM></span><span class="sxs-lookup"><span data-stu-id="6ed34-p103">OLE DB errors may be passed to your ADO application. Typically, these can be identified by a Windows facility code of <EM>4</EM>. For example, 0x800<STRONG><EM>4</EM></STRONG>.... For more information about these numbers, see Chapter 16 of the <EM>OLE DB Programmer's Reference.</EM></span></span></P>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ed34-116">Constant</span><span class="sxs-lookup"><span data-stu-id="6ed34-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="6ed34-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ed34-117">Value</span></span></p></th>
<th><p><span data-ttu-id="6ed34-118">Description</span><span class="sxs-lookup"><span data-stu-id="6ed34-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-120">3707</span><span class="sxs-lookup"><span data-stu-id="6ed34-120">3707</span></span><br />
<span data-ttu-id="6ed34-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="6ed34-121">-2146824581</span></span><br />
<span data-ttu-id="6ed34-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="6ed34-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="6ed34-123">Impossible de modifier la propriété <strong>ActiveConnection</strong> d'un objet <strong>Recordset</strong> qui possède un objet <strong>Command</strong> comme source.</span><span class="sxs-lookup"><span data-stu-id="6ed34-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-125">3732</span><span class="sxs-lookup"><span data-stu-id="6ed34-125">3732</span></span><br />
<span data-ttu-id="6ed34-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="6ed34-126">-2146824556</span></span><br />
<span data-ttu-id="6ed34-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="6ed34-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="6ed34-128">Le serveur ne peut terminer l'opération.</span><span class="sxs-lookup"><span data-stu-id="6ed34-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-130">3748</span><span class="sxs-lookup"><span data-stu-id="6ed34-130">3748</span></span><br />
<span data-ttu-id="6ed34-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="6ed34-131">-2146824540</span></span><br />
<span data-ttu-id="6ed34-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="6ed34-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p104">Connexion refusée. La nouvelle connexion demandée a des caractéristiques différentes de celle déjà en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p104">Connection was denied. New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-136">3220</span><span class="sxs-lookup"><span data-stu-id="6ed34-136">3220</span></span><br />
<span data-ttu-id="6ed34-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="6ed34-137">-2146825068</span></span><br />
<span data-ttu-id="6ed34-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="6ed34-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="6ed34-139">Le fournisseur indiqué est différent de celui utilisé.</span><span class="sxs-lookup"><span data-stu-id="6ed34-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-141">3724</span><span class="sxs-lookup"><span data-stu-id="6ed34-141">3724</span></span><br />
<span data-ttu-id="6ed34-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="6ed34-142">-2146824564</span></span><br />
<span data-ttu-id="6ed34-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="6ed34-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p105">La valeur de donnée ne peut être convertie pour des raisons autres qu'une incompatibilité de signes ou un débordement de données. Par exemple, la conversion aurait tronqué les données.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p105">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-147">3725</span><span class="sxs-lookup"><span data-stu-id="6ed34-147">3725</span></span><br />
<span data-ttu-id="6ed34-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="6ed34-148">-2146824563</span></span><br />
<span data-ttu-id="6ed34-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="6ed34-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="6ed34-150">La valeur de donnée ne peut être définie ou extraite car le type de données du champ était inconnu, ou le fournisseur ne disposait pas des ressources nécessaires pour effectuer l'opération.</span><span class="sxs-lookup"><span data-stu-id="6ed34-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-152">3747</span><span class="sxs-lookup"><span data-stu-id="6ed34-152">3747</span></span><br />
<span data-ttu-id="6ed34-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="6ed34-153">-2146824541</span></span><br />
<span data-ttu-id="6ed34-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="6ed34-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="6ed34-155">L'opération requiert un <strong>ParentCatalog</strong> valide.</span><span class="sxs-lookup"><span data-stu-id="6ed34-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-157">3726</span><span class="sxs-lookup"><span data-stu-id="6ed34-157">3726</span></span><br />
<span data-ttu-id="6ed34-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="6ed34-158">-2146824562</span></span><br />
<span data-ttu-id="6ed34-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="6ed34-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="6ed34-160">L'enregistrement ne contient pas ce champ.</span><span class="sxs-lookup"><span data-stu-id="6ed34-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-162">3421</span><span class="sxs-lookup"><span data-stu-id="6ed34-162">3421</span></span><br />
<span data-ttu-id="6ed34-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="6ed34-163">-2146824867</span></span><br />
<span data-ttu-id="6ed34-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="6ed34-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="6ed34-165">L'application utilise une valeur de type incorrect pour l'opération en cours.</span><span class="sxs-lookup"><span data-stu-id="6ed34-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-167">3721</span><span class="sxs-lookup"><span data-stu-id="6ed34-167">3721</span></span><br />
<span data-ttu-id="6ed34-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="6ed34-168">-2146824567</span></span><br />
<span data-ttu-id="6ed34-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="6ed34-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="6ed34-170">La valeur de donnée est trop grande pour être représentée par le type de données du champ.</span><span class="sxs-lookup"><span data-stu-id="6ed34-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-172">3738</span><span class="sxs-lookup"><span data-stu-id="6ed34-172">3738</span></span><br />
<span data-ttu-id="6ed34-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="6ed34-173">-2146824550</span></span><br />
<span data-ttu-id="6ed34-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="6ed34-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="6ed34-175">L'URL de l'objet à supprimer se trouve en dehors de l'étendue de l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="6ed34-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-177">3750</span><span class="sxs-lookup"><span data-stu-id="6ed34-177">3750</span></span><br />
<span data-ttu-id="6ed34-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="6ed34-178">-2146824538</span></span><br />
<span data-ttu-id="6ed34-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="6ed34-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="6ed34-180">Le fournisseur ne prend pas en charge les restrictions de partage.</span><span class="sxs-lookup"><span data-stu-id="6ed34-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-182">3751</span><span class="sxs-lookup"><span data-stu-id="6ed34-182">3751</span></span><br />
<span data-ttu-id="6ed34-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="6ed34-183">-2146824537</span></span><br />
<span data-ttu-id="6ed34-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="6ed34-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="6ed34-185">Le fournisseur ne prend pas en charge le type de restriction de partage demandé.</span><span class="sxs-lookup"><span data-stu-id="6ed34-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-187">3251</span><span class="sxs-lookup"><span data-stu-id="6ed34-187">3251</span></span><br />
<span data-ttu-id="6ed34-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="6ed34-188">-2146825037</span></span><br />
<span data-ttu-id="6ed34-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="6ed34-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="6ed34-190">Le fournisseur ou l'objet ne prend pas en charge cette opération.</span><span class="sxs-lookup"><span data-stu-id="6ed34-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-192">3749</span><span class="sxs-lookup"><span data-stu-id="6ed34-192">3749</span></span><br />
<span data-ttu-id="6ed34-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="6ed34-193">-2146824539</span></span><br />
<span data-ttu-id="6ed34-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="6ed34-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p106">Échec de la mise à jour des champs. Pour plus d'informations, examinez la propriété <strong>Status</strong> des différents objets des champs.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p106">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-198">3219</span><span class="sxs-lookup"><span data-stu-id="6ed34-198">3219</span></span><br />
<span data-ttu-id="6ed34-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="6ed34-199">-2146825069</span></span><br />
<span data-ttu-id="6ed34-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="6ed34-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="6ed34-201">L'opération n'est pas autorisée dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="6ed34-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-203">3719</span><span class="sxs-lookup"><span data-stu-id="6ed34-203">3719</span></span><br />
<span data-ttu-id="6ed34-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="6ed34-204">-2146824569</span></span><br />
<span data-ttu-id="6ed34-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="6ed34-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="6ed34-206">Le valeur de donnée entre en conflit avec les contraintes d'intégrité du champ.</span><span class="sxs-lookup"><span data-stu-id="6ed34-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-208">3246</span><span class="sxs-lookup"><span data-stu-id="6ed34-208">3246</span></span><br />
<span data-ttu-id="6ed34-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="6ed34-209">-2146825042</span></span><br />
<span data-ttu-id="6ed34-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="6ed34-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="6ed34-211">L'objet <strong>Connection</strong> ne peut être explicitement fermé pendant une transaction.</span><span class="sxs-lookup"><span data-stu-id="6ed34-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-213">3001</span><span class="sxs-lookup"><span data-stu-id="6ed34-213">3001</span></span><br />
<span data-ttu-id="6ed34-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="6ed34-214">-2146825287</span></span><br />
<span data-ttu-id="6ed34-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="6ed34-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="6ed34-216">Les arguments sont de type incorrect, en dehors des limites autorisées ou en conflit les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="6ed34-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-218">3709</span><span class="sxs-lookup"><span data-stu-id="6ed34-218">3709</span></span><br />
<span data-ttu-id="6ed34-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="6ed34-219">-2146824579</span></span><br />
<span data-ttu-id="6ed34-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="6ed34-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p107">Cette opération ne peut utiliser la connexion. Dans ce contexte, elle est soit fermée, soit non valide.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p107">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-224">3708</span><span class="sxs-lookup"><span data-stu-id="6ed34-224">3708</span></span><br />
<span data-ttu-id="6ed34-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="6ed34-225">-2146824580</span></span><br />
<span data-ttu-id="6ed34-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="6ed34-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p108">Objet <strong>Parameter</strong> défini de manière incorrecte. Des informations incohérentes ou incomplètes ont été fournies.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p108"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-230">3714</span><span class="sxs-lookup"><span data-stu-id="6ed34-230">3714</span></span><br />
<span data-ttu-id="6ed34-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="6ed34-231">-2146824574</span></span><br />
<span data-ttu-id="6ed34-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="6ed34-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="6ed34-233">La transaction de coordination n'est pas valide ou n'a pas été lancée.</span><span class="sxs-lookup"><span data-stu-id="6ed34-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-235">3729</span><span class="sxs-lookup"><span data-stu-id="6ed34-235">3729</span></span><br />
<span data-ttu-id="6ed34-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="6ed34-236">-2146824559</span></span><br />
<span data-ttu-id="6ed34-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="6ed34-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p109">L'URL contient des caractères non valides. Assurez-vous que l'URL a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p109">URL contains invalid characters. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-241">3265</span><span class="sxs-lookup"><span data-stu-id="6ed34-241">3265</span></span><br />
<span data-ttu-id="6ed34-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="6ed34-242">-2146825023</span></span><br />
<span data-ttu-id="6ed34-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="6ed34-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="6ed34-244">Impossible de trouver l'objet dans la collection correspondant au nom ou à la référence ordinale demandé(e).</span><span class="sxs-lookup"><span data-stu-id="6ed34-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-246">3021</span><span class="sxs-lookup"><span data-stu-id="6ed34-246">3021</span></span><br />
<span data-ttu-id="6ed34-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="6ed34-247">-2146825267</span></span><br />
<span data-ttu-id="6ed34-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="6ed34-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p110"><strong>BOF</strong> ou <strong>EOF</strong> est égal à True ou l'enregistrement actuel a été supprimé. L'opération demandée nécessite un enregistrement actuel.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-252">3715</span><span class="sxs-lookup"><span data-stu-id="6ed34-252">3715</span></span><br />
<span data-ttu-id="6ed34-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="6ed34-253">-2146824573</span></span><br />
<span data-ttu-id="6ed34-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="6ed34-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="6ed34-255">L'opération ne peut s'effectuer que si elle est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="6ed34-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-257">3710</span><span class="sxs-lookup"><span data-stu-id="6ed34-257">3710</span></span><br />
<span data-ttu-id="6ed34-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="6ed34-258">-2146824578</span></span><br />
<span data-ttu-id="6ed34-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="6ed34-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="6ed34-260">Impossible d'effectuer cette opération lors du traitement d'un événement.</span><span class="sxs-lookup"><span data-stu-id="6ed34-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-262">3704</span><span class="sxs-lookup"><span data-stu-id="6ed34-262">3704</span></span><br />
<span data-ttu-id="6ed34-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="6ed34-263">-2146824584</span></span><br />
<span data-ttu-id="6ed34-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="6ed34-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="6ed34-265">L'opération n'est pas autorisée tant que l'objet est fermé.</span><span class="sxs-lookup"><span data-stu-id="6ed34-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-267">3367</span><span class="sxs-lookup"><span data-stu-id="6ed34-267">3367</span></span><br />
<span data-ttu-id="6ed34-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="6ed34-268">-2146824921</span></span><br />
<span data-ttu-id="6ed34-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="6ed34-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p111">L'objet est déjà dans la collection. Impossible de l'y ajouter.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p111">Object is already in collection. Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-273">3420</span><span class="sxs-lookup"><span data-stu-id="6ed34-273">3420</span></span><br />
<span data-ttu-id="6ed34-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="6ed34-274">-2146824868</span></span><br />
<span data-ttu-id="6ed34-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="6ed34-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="6ed34-276">L'objet n'est plus valide.</span><span class="sxs-lookup"><span data-stu-id="6ed34-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-278">3705</span><span class="sxs-lookup"><span data-stu-id="6ed34-278">3705</span></span><br />
<span data-ttu-id="6ed34-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="6ed34-279">-2146824583</span></span><br />
<span data-ttu-id="6ed34-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="6ed34-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="6ed34-281">L'opération n'est pas autorisée tant que l'objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6ed34-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-283">3002</span><span class="sxs-lookup"><span data-stu-id="6ed34-283">3002</span></span><br />
<span data-ttu-id="6ed34-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="6ed34-284">-2146825286</span></span><br />
<span data-ttu-id="6ed34-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="6ed34-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="6ed34-286">Impossible d'ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="6ed34-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-288">3712</span><span class="sxs-lookup"><span data-stu-id="6ed34-288">3712</span></span><br />
<span data-ttu-id="6ed34-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="6ed34-289">-2146824576</span></span><br />
<span data-ttu-id="6ed34-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="6ed34-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="6ed34-291">Opération annulée par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ed34-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-293">3734</span><span class="sxs-lookup"><span data-stu-id="6ed34-293">3734</span></span><br />
<span data-ttu-id="6ed34-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="6ed34-294">-2146824554</span></span><br />
<span data-ttu-id="6ed34-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="6ed34-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p112">Impossible d'effectuer cette opération. Le fournisseur ne peut pas obtenir suffisamment d'espace de stockage.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p112">Operation cannot be performed. Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-299">3720</span><span class="sxs-lookup"><span data-stu-id="6ed34-299">3720</span></span><br />
<span data-ttu-id="6ed34-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="6ed34-300">-2146824568</span></span><br />
<span data-ttu-id="6ed34-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="6ed34-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="6ed34-302">Impossible d'écrire dans ce champ en raison d'une autorisation insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6ed34-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-304">3000</span><span class="sxs-lookup"><span data-stu-id="6ed34-304">3000</span></span><br />
<span data-ttu-id="6ed34-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="6ed34-305">-2146825288</span></span><br />
<span data-ttu-id="6ed34-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="6ed34-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="6ed34-307">Le fournisseur n'a pas réussi à effectuer l'opération demandée.</span><span class="sxs-lookup"><span data-stu-id="6ed34-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-309">3706</span><span class="sxs-lookup"><span data-stu-id="6ed34-309">3706</span></span><br />
<span data-ttu-id="6ed34-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="6ed34-310">-2146824582</span></span><br />
<span data-ttu-id="6ed34-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="6ed34-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p113">Fournisseur introuvable. Il peut être mal installé.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-315">3003</span><span class="sxs-lookup"><span data-stu-id="6ed34-315">3003</span></span><br />
<span data-ttu-id="6ed34-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="6ed34-316">-2146825285</span></span><br />
<span data-ttu-id="6ed34-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="6ed34-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="6ed34-318">Impossible de lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="6ed34-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-320">3731</span><span class="sxs-lookup"><span data-stu-id="6ed34-320">3731</span></span><br />
<span data-ttu-id="6ed34-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="6ed34-321">-2146824557</span></span><br />
<span data-ttu-id="6ed34-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="6ed34-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p114">Opération de copie impossible. L'objet désigné par l'URL de destination existe déjà. Spécifiez <strong>adCopyOverwrite</strong> pour remplacer l'objet.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p114">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-327">3730</span><span class="sxs-lookup"><span data-stu-id="6ed34-327">3730</span></span><br />
<span data-ttu-id="6ed34-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="6ed34-328">-2146824558</span></span><br />
<span data-ttu-id="6ed34-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="6ed34-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p115">L'objet représenté par l'URL spécifiée est verrouillé par ou plusieurs processus. Attendez la fin d'un processus et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-333">3735</span><span class="sxs-lookup"><span data-stu-id="6ed34-333">3735</span></span><br />
<span data-ttu-id="6ed34-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="6ed34-334">-2146824553</span></span><br />
<span data-ttu-id="6ed34-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="6ed34-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="6ed34-336">L'URL source ou de destination est en dehors de l'étendue de l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="6ed34-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-338">3722</span><span class="sxs-lookup"><span data-stu-id="6ed34-338">3722</span></span><br />
<span data-ttu-id="6ed34-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="6ed34-339">-2146824566</span></span><br />
<span data-ttu-id="6ed34-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="6ed34-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="6ed34-341">La valeur de donnée entre en conflit avec le type de données ou les contraintes du champ.</span><span class="sxs-lookup"><span data-stu-id="6ed34-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-343">3723</span><span class="sxs-lookup"><span data-stu-id="6ed34-343">3723</span></span><br />
<span data-ttu-id="6ed34-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="6ed34-344">-2146824565</span></span><br />
<span data-ttu-id="6ed34-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="6ed34-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="6ed34-346">La conversion a échoué car la valeur de donnée était signée alors que le type de données du champ utilisé par le fournisseur ne l'était pas.</span><span class="sxs-lookup"><span data-stu-id="6ed34-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-348">3713</span><span class="sxs-lookup"><span data-stu-id="6ed34-348">3713</span></span><br />
<span data-ttu-id="6ed34-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="6ed34-349">-2146824575</span></span><br />
<span data-ttu-id="6ed34-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="6ed34-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="6ed34-351">Opération impossible avec une connexion asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6ed34-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-353">3711</span><span class="sxs-lookup"><span data-stu-id="6ed34-353">3711</span></span><br />
<span data-ttu-id="6ed34-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="6ed34-354">-2146824577</span></span><br />
<span data-ttu-id="6ed34-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="6ed34-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="6ed34-356">Opération impossible avec une exécution asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6ed34-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-358">3728</span><span class="sxs-lookup"><span data-stu-id="6ed34-358">3728</span></span><br />
<span data-ttu-id="6ed34-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="6ed34-359">-2146824560</span></span><br />
<span data-ttu-id="6ed34-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="6ed34-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="6ed34-361">Autorisations insuffisantes pour accéder à l'arbre ou au sous-arbre.</span><span class="sxs-lookup"><span data-stu-id="6ed34-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-363">3736</span><span class="sxs-lookup"><span data-stu-id="6ed34-363">3736</span></span><br />
<span data-ttu-id="6ed34-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="6ed34-364">-2146824552</span></span><br />
<span data-ttu-id="6ed34-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="6ed34-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p116">L'opération a échoué et l'état n'est pas disponible. Le champ est peut-être indisponible ou l'opération n'a pas été tentée.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p116">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-369">3716</span><span class="sxs-lookup"><span data-stu-id="6ed34-369">3716</span></span><br />
<span data-ttu-id="6ed34-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="6ed34-370">-2146824572</span></span><br />
<span data-ttu-id="6ed34-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="6ed34-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="6ed34-372">Les paramètres de sécurité de cet ordinateur interdisent l'accès à une source de données située sur un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="6ed34-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-374">3727</span><span class="sxs-lookup"><span data-stu-id="6ed34-374">3727</span></span><br />
<span data-ttu-id="6ed34-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="6ed34-375">-2146824561</span></span><br />
<span data-ttu-id="6ed34-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="6ed34-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="6ed34-377">L'URL source ou le parent de l'URL de destination n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="6ed34-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-379">3737</span><span class="sxs-lookup"><span data-stu-id="6ed34-379">3737</span></span><br />
<span data-ttu-id="6ed34-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="6ed34-380">-2146824551</span></span><br />
<span data-ttu-id="6ed34-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="6ed34-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="6ed34-382">L'enregistrement désigné par cette URL n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="6ed34-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-384">3733</span><span class="sxs-lookup"><span data-stu-id="6ed34-384">3733</span></span><br />
<span data-ttu-id="6ed34-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="6ed34-385">-2146824555</span></span><br />
<span data-ttu-id="6ed34-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="6ed34-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p117">Le fournisseur ne peut pas localiser le périphérique de stockage indiqué par l'URL. Assurez-vous que l'URL a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p117">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-390">3004</span><span class="sxs-lookup"><span data-stu-id="6ed34-390">3004</span></span><br />
<span data-ttu-id="6ed34-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="6ed34-391">-2146825284</span></span><br />
<span data-ttu-id="6ed34-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="6ed34-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="6ed34-393">Échec de l'écriture dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="6ed34-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-395">3717</span><span class="sxs-lookup"><span data-stu-id="6ed34-395">3717</span></span><br />
<span data-ttu-id="6ed34-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="6ed34-396">-2146824571</span></span><br />
<span data-ttu-id="6ed34-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="6ed34-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p118">Utilisation interne uniquement. Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p118">For internal use only. Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="6ed34-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed34-401">3718</span><span class="sxs-lookup"><span data-stu-id="6ed34-401">3718</span></span><br />
<span data-ttu-id="6ed34-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="6ed34-402">-2146824570</span></span><br />
<span data-ttu-id="6ed34-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="6ed34-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="6ed34-p119">Utilisation interne uniquement. Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="6ed34-p119">For internal use only. Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6ed34-406">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="6ed34-406">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6ed34-407">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6ed34-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="6ed34-408">Seuls les sous-ensembles suivants d'équivalents ADO/WFC sont définis.</span><span class="sxs-lookup"><span data-stu-id="6ed34-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ed34-409">Constante</span><span class="sxs-lookup"><span data-stu-id="6ed34-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6ed34-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="6ed34-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6ed34-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="6ed34-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="6ed34-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="6ed34-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="6ed34-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="6ed34-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="6ed34-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="6ed34-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="6ed34-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="6ed34-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="6ed34-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="6ed34-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="6ed34-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="6ed34-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="6ed34-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="6ed34-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="6ed34-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed34-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="6ed34-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed34-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="6ed34-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

