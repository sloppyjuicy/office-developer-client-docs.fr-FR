---
title: Fournisseur de persistance Microsoft OLE DB (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35cab114da6536ea1a0123e0da2541dd69125824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877883"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Fournisseur de persistance Microsoft OLE DB (fournisseur de service ADO)


**S’applique à**: Access 2013, Office 2013 

Le fournisseur de persistance Microsoft OLE DB vous permet d’enregistrer un objet [Recordset](recordset-object-ado.md) dans un fichier ultérieurement restaurer cet objet **Recordset** à partir du fichier. Informations de schéma, les données et les modifications en attente sont conservés.

Vous pouvez enregistrer le **Recordset** au format ADTG (Advanced Data Table Gram) ou au format XML ouvert (Extensible Markup Language).

## <a name="provider-keyword"></a>Mot clé du fournisseur

Pour appeler ce fournisseur, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Erreurs

Les erreurs suivantes émises par ce fournisseur peuvent être détectées dans votre application.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>Le fichier ouvert n'a pas un format valide (c'est-à-dire que son format n'est ni ADTG, ni XML ).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>L'objet <strong>Recordset</strong> enregistré présente des caractéristiques qui l'empêchent d'être stocké.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Le fournisseur de persistance Microsoft OLE DB n'expose pas de propriétés dynamiques.

Actuellement, seuls les objets **Recordset** hiérarchiques paramétrés ne peuvent pas être enregistrés.

Pour plus d'informations sur le stockage persistant des objets **Recordset**, consultez la rubrique [Informations complémentaires sur la persistance des objets Recordset](more-about-recordset-persistence.md).

Lorsqu’un flux est utilisé pour ouvrir un **Recordset**, il doit y avoir aucun paramètre spécifié le paramètre *Source* de la méthode **Open** .

