---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Utilisez le modèle URI balancement pour ouvrir l’application balancement et afficher ou modifier un balancement.
ms.openlocfilehash: 7a820339abcd666e7e1b9ad584cd152ca8fd4f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787999"
---
# <a name="sway-uri-scheme"></a>Modèle URI de balancement

Ce document définit le format d’Uniform Resource Identifier (URI) pour l’application de balancement pour Windows. Vous pouvez utiliser ce modèle URI pour invoquer l’application balancement avec différentes commandes.

## <a name="sway-uri-scheme-syntax"></a>La syntaxe de schéma URI de balancement

Voici la syntaxe de schéma URI :

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indique que balancement est l’application à appeler. Lorsque balancement pour Windows est installé, `ms-sway` est enregistré avec Windows pour le Gestionnaire de balancement.
- `<command-argument>`&ndash; URI A peut-être un ou plusieurs arguments de commande, délimité par le signe (`&`) caractères. Lorsque plusieurs arguments de commande est inclus dans un URI, une esperluette (`&`) caractère doit séparer chaque argument de commande de l’argument de commande suivant. Arguments de la commande varient en fonction du scénario. 

## <a name="command-arguments"></a>Arguments de la commande

Plusieurs arguments de la commande peuvent être inclus dans le schéma d’URL balancement. Ces arguments de commande ne sont pas nécessaires. Si vous n’incluez pas les arguments de commande, l’application balancement est appelée.

|Nom de l’argument commande|Description|Type|Valeurs possibles|Obligatoire ?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Identificateur unique d’un balancement. Utilisé pour indiquer le balancement à ouvrir.|Chaîne|Valide un identificateur unique pour un balancement. L’id est toujours partie de l’URL à un balancement.<br/><br/>Par exemple, pour le balancement suivant `https://sway.com/dBheQgVZ1RQBfiQU`, l’id est `dBheQgVZ1RQBfiQU`.<br/><br/>Si le compte d’utilisateur associé à l’application balancement possède des autorisations de modification, l’application s’ouvre le balancement en mode édition. Dans le cas contraire, l’application s’ouvre le balancement en mode d’affichage.|Non|
|**mode**|Le mode dans lequel un balancement spécifique doit être ouvert, si pour l’édition ou affichage.|Chaîne|edit<br/>view<br/><br/>**Remarque**: Si aucun **id** n’est spécifié, cet argument de commande est ignoré.|Non|
|**auth_upn**|Le compte à utiliser lors de l’ouverture de balancement.|Chaîne|Une adresse de messagerie valide.<br/><br/>Si l’adresse de messagerie spécifiée n’est pas associé à un compte balancement, balancement invite l’utilisateur à se connecter en tant que l’utilisateur spécifié.<br/><br/>Si plus d’un compte est associé à l’application de balancement et l’adresse de messagerie spécifiée existe, l’application balancement passe à l’aide de ce compte lorsqu’il est appelé.|Non|
|**authentification\_pvr**|Le type de compte à utiliser pour ouvrir le balancement&mdash;un compte Microsoft ou un compte Azure Active Directory (AD Azure).|Chaîne|WindowsLiveId – indique que le **auth\_upn** compte est un compte Microsoft.<br/><br/>OrgId – indique que le **auth\_upn** compte est un compte Azure AD.<br/><br/>Si aucune **auth\_upn** est spécifié, cet argument de commande est ignoré.|Non|
|**appel\_application**|Le nom de l’application Windows utilisée pour invoquer balancement.|Chaîne|Le nom convivial de l’application Windows utilisée pour invoquer balancement via le modèle d’URL balancement.<br/><br/>L’objectif de cet argument de commande est de télémétrie et de suivi.|Non|

## <a name="uri-scheme-semantics"></a>Sémantique de schéma URI

Le `<ms-sway>` schéma définit une syntaxe d’URI pour l’ouverture d’un balancement ou pour appeler l’application balancement. Le schéma définit plusieurs arguments de commande, qui peuvent être utilisés pour effectuer les opérations suivantes : 

- Ouvrez l’application balancement &ndash; sans argument de commande doit être spécifiés. 

- Ouvrez un balancement pour l’afficher dans l’application balancement &ndash; **l’id** et le **mode** afficher la valeur doivent être spécifiés. 

- Ouvrir un balancement pour modification dans l’application balancement &ndash; **l’id** et le **mode** défini sur Modifier doit être spécifié. Nous vous recommandons également inclure **auth\_upn** et **auth\_pvr** pour s’assurer que le compte avec des autorisations de modification de droite est utilisé lorsque balancement est ouvert.  

## <a name="example"></a>Exemples

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


