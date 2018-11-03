---
title: Initialisation du pilote de source de données Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6e1d61d2f61050118745347441cba1f27c35c41f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937742"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Initialisation du pilote de source de données Microsoft Exchange

**S’applique à**: Access 2013, Office 2013

Lorsque vous installez le pilote de Source de données Microsoft Exchange, le programme d’installation écrit un ensemble de valeurs par défaut dans les sous-clés et ISAM Formats du Registre Microsoft Windows. Vous ne devez pas modifier ces paramètres directement. Utilisez le programme d’installation pour votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l’initialisation et les paramètres de Format ISAM pour le pilote de Source de données Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Paramètres d'initialisation de source de données Microsoft Exchange

Le **Access Connectivity Engine\\moteurs\\Exchange** dossier contient des paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange. L'unique entrée dans ce dossier est la suivante :

`win32=<path>\ACEEXCH.DLL`

Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll. Le chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type de Registre\_SZ.

Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.

## <a name="microsoft-outlook-client-isam-formats"></a>Formats ISAM du client Microsoft Outlook

Le **Access Connectivity Engine\\Formats ISAM\\Outlook 9.0** dossier contient les entrées suivantes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données pour que les nouveaux paramètres soient appliqués.



## <a name="microsoft-exchange-client-isam-formats"></a>Formats ISAM du client Microsoft Exchange

Le **Access Connectivity Engine\\Formats ISAM\\Exchange 4.0** dossier contient les entrées suivantes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données afin que les nouveaux paramètres prennent effet.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Personnalisation du fichier schema.ini pour les données Outlook et Exchange

Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.

Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.

