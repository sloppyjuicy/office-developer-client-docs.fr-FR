---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Utilisez le modèle d'URI Sway pour ouvrir l'application Sway et afficher ou modifier un Sway.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346248"
---
# <a name="sway-uri-scheme"></a>Modèle d’URI Sway

Ce document définit le format des URI (Uniform Resource Identifier) de l'application Sway pour Windows. Vous pouvez utiliser ce modèle d'URI pour appeler l'application Sway avec différentes commandes.

## <a name="sway-uri-scheme-syntax"></a>Syntaxe de modèle d'URI Sway

La syntaxe du modèle d'URI est la suivante:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indique que Sway est l'application à appeler. Lorsque Sway pour Windows est installé, `ms-sway` il est inscrit auprès de Windows pour être le gestionnaire Sway.
- `<command-argument>`&ndash; Un URI peut avoir un ou plusieurs arguments de commande, délimités par le`&`signe «perluète» (). Lorsque plusieurs arguments de commande sont inclus dans un URI, un caractère perluète (`&`) doit séparer chaque argument de commande de l'argument de commande suivant. Les arguments de la commande varient en fonction du scénario. 

## <a name="command-arguments"></a>Arguments de commande

Plusieurs arguments de commande peuvent être inclus dans le modèle d'URL Sway. Ces arguments de commande ne sont pas obligatoires. Si vous n'incluez pas les arguments de commande, l'application Sway est appelée.

|Nom de l'argument de la commande|Description|Type|Valeurs possibles|Obligatoire ?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Identificateur unique d'un Sway. Permet d'indiquer le Sway à ouvrir.|String|Identificateur unique valide pour un Sway. L'ID fait toujours partie de l'URL vers un Sway.<br/><br/>Par exemple, pour le Sway `https://sway.com/dBheQgVZ1RQBfiQU`suivant, l'ID est `dBheQgVZ1RQBfiQU`.<br/><br/>Si le compte d'utilisateur associé à l'application Sway dispose des autorisations de modification, l'application ouvre le Sway en mode édition. Dans le cas contraire, l'application ouvre le Sway en mode affichage.|Non|
|**mode**|Mode dans lequel un Sway spécifique doit être ouvert, qu'il s'agisse de modifier ou d'afficher.|String|edit<br/>view<br/><br/>**Remarque**: si aucun **ID** n'est spécifié, cet argument de commande est ignoré.|Non|
|**auth_upn**|Compte à utiliser lors de l'ouverture de Sway.|String|Adresse de messagerie valide.<br/><br/>Si l'adresse de messagerie spécifiée n'est pas associée à un compte Sway, Sway demande à l'utilisateur de se connecter en tant qu'utilisateur spécifié.<br/><br/>Si plusieurs comptes sont associés à l'application Sway et que l'adresse de messagerie spécifiée existe, l'application Sway bascule vers l'utilisation de ce compte lorsqu'elle est appelée.|Non|
|**PVR\_auth**|Type de compte à utiliser pour ouvrir le Sway&mdash;soit un compte Microsoft, soit un compte Azure Active Directory (Azure AD).|String|WindowsLiveId: spécifie que le compte **UPN auth\_** est un compte Microsoft.<br/><br/>OrgId: spécifie que le compte **UPN auth\_** est un compte Azure ad.<br/><br/>Si aucun **nom\_d'utilisateur principal auth** n'est spécifié, cet argument de commande est ignoré.|Non|
|**appel\_de l'application**|Nom de l'application Windows utilisée pour appeler Sway.|String|Nom convivial de l'application Windows utilisée pour appeler Sway via le modèle d'URL Sway.<br/><br/>L'objet de cette commande est pour la télémétrie et le suivi.|Non|

## <a name="uri-scheme-semantics"></a>Sémantique de modèle d'URI

Le `<ms-sway>` modèle définit une syntaxe d'URI pour l'ouverture d'un Sway ou pour l'appel de l'application Sway. Le modèle définit plusieurs arguments de commande, qui peuvent être utilisés pour effectuer les opérations suivantes: 

- Ouvrir l'application &ndash; Sway aucun argument de commande ne doit être spécifié. 

- Ouvrir un Sway pour l'affichage dans l'application &ndash; Sway l' **ID** et le **mode** définis sur View doivent être spécifiés. 

- Ouvrir un Sway pour modification dans l'application &ndash; Sway l' **ID** et le **mode** définis sur modifier doivent être spécifiés. Nous vous recommandons également d'inclure **l'\_UPN auth** et les **PVR auth\_** pour vous assurer que le compte approprié avec des autorisations de modification est utilisé lors de l'ouverture de Sway.  

## <a name="example"></a>Exemple

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


