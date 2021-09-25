---
title: Solutions pour l'accès à distance aux données
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c9b0256e71915df442954fd0b4c5d1625e03b218
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617425"
---
# <a name="solutions-for-remote-data-access"></a>Solutions pour l’accès aux données distant

**S’applique à** : Access 2013, Office 2013

## <a name="the-issue"></a>Le problème

ADO permet à votre application d'accéder directement aux sources de données et de les modifier (système à deux couches). Par exemple, si vous êtes connecté à la source de données qui contient vos données, il s'agit d'une connexion directe dans un système à deux couches.

Toutefois, vous souhaitez peut-être accéder aux sources de données indirectement via un intermédiaire tel que Microsoft Internet Information Services (IIS). Ce type de système est parfois appelé système à trois couches. IIS est un système client/serveur qui fournit à une application locale ou cliente un moyen efficace d'appeler un programme distant (serveur) sur Internet ou dans un intranet. Le programme serveur accède à la source des données et traite éventuellement les données acquises.

Par exemple, votre page web intranet contient une application écrite en Microsoft Visual Basic Scripting Edition (VBScript), qui se connecte à IIS. IIS se connecte à son tour à la source de données, extrait les données et les traite d'une façon quelconque, puis retourne les informations traitées à votre application.

Dans cet exemple, votre application ne se connecte jamais directement à la source de données ; c'est IIS qui s'y connecte et accède aux données par l'intermédiaire d'ADO.

> [!NOTE]
> L’application client/serveur n’a pas besoin d’être basée sur Internet ou sur un intranet (c’est-à-dire, basé sur le web) ; elle peut se composer uniquement de programmes compilés sur un réseau local. Toutefois, le cas type est une application web.

Dans la mesure où certains contrôles visuels, tels que les grilles, les cases à cocher ou les listes, sont susceptibles d'utiliser les informations retournées, ils doivent être en mesure de les manipuler facilement.

Si vous voulez une interface de programmation d'application simple et efficace, capable de prendre en charge les systèmes à trois couches et de renvoyer les informations comme si elles avaient été extraites d'un système à deux couches, l'interface RDS (Remote Data Service) est l'interface qu'il vous faut.

## <a name="the-solution"></a>La solution

RDS définit un modèle de programmation( la séquence d’activités nécessaire pour accéder à une source de données et la mettre à jour) pour accéder aux données par le biais d’un intermédiaire, tel que Internet Information Services (IIS). Le modèle de programmation résume toutes les fonctionnalités de l'interface RDS.

