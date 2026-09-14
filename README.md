#  Detailed Error / Failure Analysis

## Error Analysis

The worst CNN predictions were selected using reconstruction error and inspected individually.

The analysis focused on:
- Low-visibility scenes
- Low-contrast regions
- Color differences
- Loss of fine details
- Complex underwater scenes

## Observed Limitations

1. The CNN may struggle with severely degraded underwater images.
2. Fine edges and small details may not always be recovered accurately.
3. Some outputs may still show color differences compared with the target.
4. Complex scenes can produce incomplete enhancement.
5. The limited number of paired training images can restrict generalization.

## Likely Failure Conditions

The model is more likely to produce weaker results when:
- The input image is extremely dark.
- Contrast is very low.
- Important structures are very small.
- The scene contains complex visual details.
- The input-target appearance difference is large.

## Research Insight

The CNN provides stronger overall reconstruction performance according to PSNR and SSIM, while the refined CLAHE-3 method provides stronger edge preservation. This shows that underwater enhancement involves a trade-off between overall image similarity and structural detail preservation.

## Conclusion

The failure analysis identifies difficult scenes and remaining weaknesses of the CNN.
