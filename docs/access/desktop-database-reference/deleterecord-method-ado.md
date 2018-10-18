---
title: DeleteRecord, méthode (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a91da1304d399a34f247eb251c2dadf0f1fa94d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603006"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013



Supprime une entité représentée par un objet [Record](record-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Enregistrement*. **DeleteRecord *** Source*, *asynchrone*

## <a name="parameters"></a>Paramètres

  - *Source*

  - Facultatif. Valeur de type **String** contenant l’URL qui identifie l’entité (par exemple, le fichier ou le répertoire) à supprimer. Si le paramètre *Source* est omis ou spécifie une chaîne vide, l’entité représentée par l’objet [Record](record-object-ado.md) actif est supprimée. Si l’objet Record est un enregistrement de collection (propriété [RecordType](recordtype-property-ado.md) avec la valeur **adCollectionRecord**, tel qu’un répertoire) tous les enfants (par exemple les sous-répertoires) seront également supprimés.

  - *Async*

  - Facultatif. Valeur de type **Boolean**. Si sa valeur est **True**, spécifie que l'opération de suppression est asynchrone.

## <a name="remarks"></a>Notes

Opérations sur l’objet représenté par cet **enregistrement** peuvent échouer une fois cette méthode terminée. Après avoir appelé **DeleteRecord**, l' **enregistrement** doit être fermé car le comportement de l' **enregistrement** peut devenir imprévisible selon le moment où le fournisseur met à jour l' **enregistrement** de la source de données.

Si cet **enregistrement** a été obtenue à partir d’un [jeu d’enregistrements](recordset-object-ado.md), puis les résultats de cette opération ne seront pas reflétées immédiatement dans le **jeu d’enregistrements**. Actualiser le **jeu d’enregistrements** en fermant et en ouvrant de nouveau ou en exécutant les méthodes **Recordset** [Requery](requery-method-ado.md)ou [Update](update-method-ado.md) et [Resync](resync-method-ado.md) .


> [!NOTE]
<<<<<<< Tête
> <P>[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>
=======
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).
>>>>>>> master


