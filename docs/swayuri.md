---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Utilisez le schéma d’URI Sway pour ouvrir l’application Sway et afficher ou modifier un Sway.
ms.openlocfilehash: fb558a4d00d411f58c8b16fc76d021a6403ed4d5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783795"
---
# <a name="sway-uri-scheme"></a>Modèle d’URI Sway

Ce document définit le format des  URL (Uniform Resource Identifiers) pour l’application Sway pour Windows. Vous pouvez utiliser ce schéma d’URI pour appeler l’application Sway avec différentes commandes.

## <a name="sway-uri-scheme-syntax"></a>Syntaxe du schéma d’URI Sway

Voici la syntaxe du schéma d’URI :

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indique que Sway est l’application à appeler. Lorsque Sway pour Windows est installé, `ms-sway` est inscrit auprès de Windows en être le handler Sway.
- `<command-argument>`&ndash; Un URI peut avoir un ou plusieurs arguments de commande, délimités par le caractère « ampersand » (`&`). Lorsque plusieurs arguments de commande sont inclus dans un URI, un caractère « eter » (`&`) doit séparer chaque argument de commande de l’argument de commande suivant. Les arguments de commande varient en fonction du scénario. 

## <a name="command-arguments"></a>Arguments de commande

Plusieurs arguments de commande peuvent être inclus dans le schéma d’URL Sway. Ces arguments de commande ne sont pas obligatoires. Si vous n’incluez pas les arguments de commande, l’application Sway est invoquée.

|Nom de l’argument de commande|Description|Type|Valeurs possibles|Obligatoire ?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Identificateur unique d’un Sway. Utilisé pour indiquer le Sway à ouvrir.|String|Identificateur unique valide pour un Sway. L’ID fait toujours partie de l’URL d’un Sway.<br/><br/>Par exemple, pour le Sway suivant `https://sway.com/dBheQgVZ1RQBfiQU`, l’ID est `dBheQgVZ1RQBfiQU`.<br/><br/>Si le compte d’utilisateur associé à l’application Sway dispose d’autorisations de modification, l’application ouvre le Sway en mode édition. Dans le cas contraire, l’application ouvre le Sway en mode d’affichage.|Non|
|**mode**|Mode dans lequel un Sway spécifique doit être ouvert, que ce soit pour la modification ou pour l’affichage.|String|edit<br/>view<br/><br/>**REMARQUE** : si aucun **ID** n’est spécifié, cet argument de commande est ignoré.|Non|
|**auth_upn**|Compte à utiliser lors de l’ouverture de Sway.|String|Adresse de messagerie valide.<br/><br/>Si l’adresse de messagerie spécifiée n’est pas associée à un compte Sway, Sway demande à l’utilisateur de se connecter en tant qu’utilisateur spécifié.<br/><br/>Si plusieurs comptes sont associés à l’application Sway et que l’adresse de messagerie spécifiée existe, l’application Sway bascule vers l’utilisation de ce compte lorsqu’elle est invoquée.|Non|
|**authpvr\_**|Type de compte à utiliser pour ouvrir le Swayeither&mdash; un compte Microsoft ou un Azure Active Directory (Azure AD).|String|WindowsLiveId : spécifie que le compte **authupn\_** est un compte Microsoft.<br/><br/>OrgId : spécifie que le compte **authupn\_** est un Azure AD client.<br/><br/>Si aucune **thupn\_ n’est** spécifiée, cet argument de commande est ignoré.|Non|
|**invokingapp\_**|Nom de l’application Windows utilisée pour appeler Sway.|String|Nom convivial de l’application Windows utilisée pour appeler Sway via le schéma d’URL Sway.<br/><br/>L’objectif de cet argument de commande est la télémétrie et le suivi.|Non|

## <a name="uri-scheme-semantics"></a>Sémantique du schéma d’URI

Le `<ms-sway>` schéma définit une syntaxe d’URI pour l’ouverture d’une Sway ou l’appel de l’application Sway. Le schéma définit plusieurs arguments de commande, qui peuvent être utilisés pour : 

- Ouvrez l’application &ndash; Sway Aucun argument de commande n’a besoin d’être spécifié. 

- Ouvrez un Sway pour l’afficher dans l’application &ndash; Sway **L’ID** et le **mode** à afficher doivent être spécifiés. 

- Ouvrez un Sway pour modification dans l’application &ndash; Sway **L’ID** et le **mode** de modification doivent être spécifiés. Nous vous recommandons d’inclure également **authupn\_** et **authpvr\_** pour vous assurer que le bon compte avec des autorisations de modification est utilisé lors de l’ouverture de Sway.  

## <a name="example"></a>Exemple

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp`
