---
title: '@viewport'
slug: Web/CSS/@viewport
tags:
  - CSS
  - Experimental
  - Reference
  - Règle @
translation_of: Web/CSS/@viewport
---
{{SeeCompatTable}}{{CSSRef}}

La règle @** `@viewport`** permet de configurer la zone d'affichage (le _viewport_ en anglais) à travers laquelle le document est affiché. Cette règle est principalement utilisée pour les appareils mobiles mais aussi pour les navigateurs de bureau (par exemple Microsoft Edge qui gère la division de l'écran).

Les longueurs exprimées en pourcentages sont calculées de façon relative à la **zone d'affichage initiale** c'est-à-dire le _viewport_ avant tout ajustement effectué par le navigateur ou par les styles de la page. Généralement, cela correspond à la taille de la fenêtre pour les navigateurs de bureau lorsqu'ils ne sont pas utilisés en mode plein écran.

Pour les appareils mobiles (ou pour les appareils de bureau qui sont en plein écran), la zone d'affichage initiale correspond à la portion de l'écran disponible pour l'application. Cela peut correspondre à l'écran entier ou bien à l'écran auquel on enlève les zones contrôlées par le système d'exploitation (par exemple la barre de tâche) ou bien encore à la zone de l'écran qui n'est pas occupée par le système d'exploitation ou d'autres applications.

```css
@viewport {
  width: device-width;
}
```

## Syntaxe

Cette règle @ contient un ensemble de descripteurs CSS dans un bloc délimité par des accolades.

Un facteur de zoom de `1.0` ou de `100%` signifie qu'il n'y a eu aucun zoom. Si la valeur est supérieure, cela signifie qu'on a zoomé pour agrandir le contenu. Inversement, si la valeur est inférieure à `1.0` ou à `100%`, cela signifie qu'on a dézoomé.

### Descripteurs

Les navigateurs sont supposés ignorer les descripteurs non reconnus.

- {{cssxref("@viewport/min-width","min-width")}}
  - : Ce descripteur détermine la largeur minimale de la zone d'affichage (_viewport_) lorsque le document est affiché initialement.
- {{cssxref("@viewport/max-width","max-width")}}
  - : Ce descripteur détermine la largeur maximale de la zone d'affichage (_viewport_) lorsque le document est affiché initialement.
- {{cssxref("@viewport/width","width")}}
  - : Ce descripteur est un raccourci qui permet de définir `min-width` et `max-width`.
- {{cssxref("@viewport/min-height","min-height")}}
  - : Ce descripteur détermine la hauteur minimale de la zone d'affichage (_viewport_) lorsque le document est affiché initialement.
- {{cssxref("@viewport/max-height","max-height")}}
  - : Ce descripteur détermine la hauteur maximale de la zone d'affichage (_viewport_) lorsque le document est affiché initialement.
- {{cssxref("@viewport/height","height")}}
  - : Ce descripteur est un raccourci qui permet de définir `min-height` et `max-height`.
- {{cssxref("@viewport/zoom","zoom")}}
  - : Ce descripteur permet de définir le niveau de zoom initial.
- {{cssxref("@viewport/min-zoom","min-zoom")}}
  - : Ce descripteur permet de définir le niveau de zoom minimal.
- {{cssxref("@viewport/max-zoom","max-zoom")}}
  - : Ce descripteur permet de définir le niveau de zoom maximal.
- {{cssxref("@viewport/user-zoom","user-zoom")}}
  - : Ce descripteur indique si l'utilisateur peut, ou non, changer le niveau de zoom.
- {{cssxref("@viewport/orientation","orientation")}}
  - : Ce descripteur contrôle l'orientation du document.
- {{cssxref("@viewport/ viewport-fit", "viewport-fit")}}
  - : Ce descripteur contrôle l'affichage du document pour les affichages non-rectangulaires.

> **Note :**Un facteur de zoom de `1.0` ou `100%` correspond à une absence de zoom. Les valeurs supérieures traduiront une augmentation du niveau de zoom (agrandissement des images et du texte) et les valeurs inférieures correspondront à une réduction du niveau de zoom.

### Syntaxe formelle

{{csssyntax}}

## Exemples

```css
@viewport {
  min-width: 640px;
  max-width: 800px;
}

@viewport {
  zoom: 0.75;
  min-zoom: 0.5;
  max-zoom: 0.9;
}

@viewport {
  orientation: landscape;
}
```

## Spécifications

| Spécification                                                                                        | État                                     | Commentaires                                                                                        |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------- |
| {{SpecName("CSS Round Display", "#extending-viewport-rule", "@viewport")}} | {{Spec2("CSS Round Display")}} | Définition du descripteur {{cssxref("@viewport/viewport-fit", "viewport-fit")}}. |
| {{SpecName('CSS3 Device', '#the-atviewport-rule', '@viewport')}}                 | {{Spec2('CSS3 Device')}}         | Définition initiale.                                                                                |

## Compatibilité des navigateurs

{{Compat("css.at-rules.viewport")}}

## Voir aussi

- {{HTMLElement("meta")}} et plus précisément `<meta name="viewport">`
- [Utiliser la balise `meta` afin de contrôler la disposition sur les navigateurs mobiles](/fr/docs/Mozilla/Mobile/Balise_meta_viewport)